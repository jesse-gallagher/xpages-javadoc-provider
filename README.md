# XPages Javadoc Contributor

This project contains a plugin for Eclipse and Domino Designer that provides Javadoc for several of the standard libraries present in the XPages stack.

This Javadoc is specifically the published documentation referenced [in the Domino Designer wiki](https://ds_infolib.hcltechsw.com/ldd/ddwiki.nsf/dx/Domino_Designer_Extensibility_APIs_Javadoc_9.0.1), with the information corresponding to Domino 9.0.1.

Currently, the Javadoc is referenced via its hosted location on IBM's software servers and thus it is possible that they will remove it at any time. If HCL hosts the documentation on their side (or licenses it for redistribution), I will be able to change this project to not depend on IBM.

## Installation and Usage

In Designer, this can be installed via File -> Application -> Install. In a fresh Designer installation, you will have to [alter the Target Platform](https://frostillic.us/blog/posts/2018/10/19/abstractcompiledpage--missing-plugins--and-manifest.mf-in-fp10-and-v10) to reference installed custom plug-ins.

In Eclipse, this can vbe installed via Help -> Install New Software. In addition, the provider bundle (`org.openntf.xsp.javadoc.provider_xx.jar` in the update site) must be present in your Target Platform. You can do this either by including your current Eclipse installation in your Target Platform (as in the default "Running Platform" target), adding the Update Site from this project to your Target Platform, or copying the bundle into your XPages update site (such as one generated via [`generate-domino-update-site`](https://openntf.org/main.nsf/project.xsp?r=project/Domino%20Update%20Site%20Generator)).

Once installed, Javadoc for the covered classes should automatically appear when using bundle dependencies in a PDE (plug-in) project or an NSF:

![Screenshot showing inline Javadoc for the XspLibrary class](img/example.png)

On first use, it may take a few moments for the remote Javadoc to load.

## Coverage

The libraries that have some or all of their classes covered in the published Javadoc are:

- com.ibm.commons
- com.ibm.commons.iloader
- com.ibm.commons.jdbc
- com.ibm.commons.swt
- com.ibm.commons.swt.data
- com.ibm.commons.xml
- com.ibm.designer.domino.ide.resources
- com.ibm.designer.domino.scripting
- com.ibm.designer.domino.xsp.editor
- com.ibm.designer.domino.xsp.editor
- com.ibm.xsp.core
- com.ibm.xsp.designer
- com.ibm.xsp.domino