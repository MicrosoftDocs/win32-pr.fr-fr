---
description: Un assembly privé est un assembly qui est déployé avec une application et qui est disponible pour l’utilisation exclusive de cette application.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: À propos des assemblys privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238181"
---
# <a name="about-private-assemblies"></a>À propos des assemblys privés

Un assembly privé est un assembly qui est déployé avec une application et qui est disponible pour l’utilisation exclusive de cette application. Autrement dit, les autres applications ne partagent pas l’assembly privé. Les assemblys privés sont l’une des méthodes qui peuvent être utilisées pour créer des [applications isolées](isolated-applications.md). Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](about-isolated-applications-and-side-by-side-assemblies.md).

Les assemblys privés doivent être conçus pour fonctionner côte à côte avec d’autres versions de l’assembly sur le système. Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).

Les assemblys privés doivent être accompagnés d’un [manifeste d’assembly](assembly-manifests.md). notez que des restrictions de nom s’appliquent lors de l’empaquetage d’une DLL en tant qu’assembly privé pour s’adapter à la façon dont Windows recherche les assemblys privés. Lors de la recherche d’assemblys privés, la méthode recommandée consiste à inclure le manifeste d’assembly dans la DLL en tant que ressource. Dans ce cas, l’ID de ressource doit être égal à 1 et le nom de l’assembly privé peut être le même que le nom de la DLL. Par exemple, si le nom de la DLL est MICROSOFT.WINDOWS.MYSAMPLE.DLL, la valeur de l’attribut Name utilisé dans l’élément **assemblyIdentity** du manifeste peut également être Microsoft. Windows. mysample. Une autre méthode de recherche d’assemblys privés consiste à fournir le manifeste de l’assembly dans un fichier séparé. Dans ce cas, le nom de l’assembly et son manifeste doivent être différents du nom de la DLL. Par exemple, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest et Microsoft.Windows.mysample.dll. Pour plus d’informations sur la façon dont les recherches côte à côte pour les assemblys privés, consultez [séquence de recherche](assembly-searching-sequence.md)d’assemblys.

Les assemblys privés sont installés dans un dossier de la structure de répertoires de l’application. En règle générale, il s’agit du dossier contenant le fichier exécutable de l’application. Les assemblys privés peuvent être déployés dans le même dossier que l’application, dans un dossier portant le même nom que l’assembly, ou dans un sous-dossier spécifique à une langue portant le même nom que l’assembly. Par exemple, utilisez l’une des structures de répertoire suivantes pour déployer un assembly privé, Microsoft. Tools. pop, sans langue spécifiée.



| Structure de répertoires                                       | Description                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| APPDIR \\MICROSOFT.TOOLS.POP.DLL                           | Le manifeste est déployé en tant que ressource dans la DLL.                                                     |
| Appdir \\ Microsoft. Tools. pop. manifest                      | Le manifeste est déployé en tant que fichier distinct.                                                           |
| APPDIR \\ Microsoft. Tools. \\MICROSOFT.TOOLS.POP.DLL pop      | Le manifeste est déployé en tant que ressource dans la DLL, qui se trouve dans un sous-dossier portant le nom de l’assembly. |
| Appdir \\ Microsoft. Tools. pop \\ Microsoft. Tools. pop. manifest | Le manifeste est déployé en tant que fichier distinct dans un sous-dossier portant le nom de l’assembly.                 |



 

> [!IMPORTANT]
>
> pour les versions du système d’exploitation Windows avant Windows 7 et Windows Server 2008 R2, les assemblys privés natifs doivent être déployés dans le dossier qui contient le fichier exécutable de l’application. L’installation dans un dossier spécifique à une langue ou dans le dossier portant le même nom que l’assembly n’est pas prise en charge pour les assemblys privés natifs.

 

Utilisez l’une des structures de répertoire suivantes pour déployer un assembly privé, Microsoft. Tools. pop, avec la langue spécifiée. Dans l’exemple suivant, la langue utilisée par Microsoft. Tools. pop est l’anglais (États-Unis) et le code de langue est en-US. Vous devez substituer le code de langue DHTML approprié à votre assembly.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Les assemblys privés peuvent être installés par n’importe quelle méthode d’installation qui peut copier le fichier de l’assembly dans ce dossier, tel que la commande **xcopy** . pour plus d’informations sur l’installation d’assemblys privés à l’aide de la Windows Installer, consultez [Installation d’assemblys Win32](../msi/installation-of-win32-assemblies.md).

les assemblys privés peuvent également être installés sur des systèmes d’exploitation antérieurs à Windows XP. Dans ce cas, l’assembly doit être enregistré et, sur ces systèmes d’exploitation, le manifeste n’est pas utilisé. Une copie de l’assembly privé est installée dans un dossier privé pour l’utilisation exclusive de l’application. Une autre version de l’assembly peut être inscrite globalement sur le système et disponible pour toutes les applications qui y sont liées. La version globale de l’assembly peut être la version installée avec l’application ou une version antérieure. Pour plus d’informations, consultez [redirection DLL/com sur Windows](dll-com-redirection-on-windows.md). Un assembly peut également être installé en tant qu’assembly partagé pour une utilisation par plusieurs applications. Pour plus d’informations, consultez [assemblys partagés](/windows/desktop/Msi/shared-assemblies).

Notez que les étapes de création d’un assembly privé sont identiques à celles de la création d’un assembly partagé, à deux exceptions près :

-   Un assembly privé n’a pas besoin d’être signé et **publickeyToken** n’est pas requis dans l’élément **assemblyIdentity** du manifeste de l’assembly.
-   Les assemblys privés peuvent être installés dans le dossier de l’application à l’aide de n’importe quelle technologie d’installation. il n’est pas nécessaire d’installer les assemblys privés à l’aide de l’Windows Installer.

 

 
