---
description: Un fichier de configuration d’application est un fichier XML utilisé pour contrôler la liaison d’assembly.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Fichiers de configuration des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112718"
---
# <a name="application-configuration-files"></a>Fichiers de configuration des applications

Un fichier de configuration d’application est un fichier XML utilisé pour contrôler la liaison d’assembly. Il peut rediriger une application de à l’aide d’une version d’un assembly côte à côte vers une autre version du même assembly. C’est ce que l’on appelle [une configuration par application](per-application-configuration.md). Un fichier de configuration d’application s’applique uniquement à un manifeste d’application spécifique et aux assemblys dépendants. Les composants isolés compilés avec un manifeste d’ID de ressource de manifeste ISOLATIONAWARE incorporé \_ \_ \_ nécessitent un fichier de configuration d’application distinct. Les manifestes gérés avec [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) nécessitent un fichier de configuration d’application distinct.

La redirection spécifiée par un fichier de configuration de l’application peut remplacer les versions d’assembly spécifiées par les [manifestes d’application](application-manifests.md) et les [fichiers de configuration](publisher-configuration-files.md)du serveur de publication. Par exemple, si un fichier de configuration d’éditeur spécifie que toutes les références à un assembly doivent être redirigées de la version 1.0.0.0 vers 1.1.0.0, un fichier de configuration d’application peut être utilisé pour rediriger une application spécifique afin d’utiliser la version 1.0.0.0. Un fichier de configuration d’application s’applique uniquement au manifeste d’application et aux assemblys dépendants spécifiés.

Pour obtenir une liste complète du schéma XML, consultez [schéma du fichier de configuration](application-configuration-file-schema.md)de l’application.

Les éléments et les attributs des fichiers de configuration de l’application sont répertoriés dans le tableau suivant.



| Élément               | Attributs                | Obligatoire |
|-----------------------|---------------------------|----------|
| **configuration**     |                           | Oui      |
| **windows**           |                           | Oui      |
| **publisherPolicy**   |                           | Oui      |
|                       | **appliqu**                 | Oui      |
| **Language**           |                           | Non       |
| **assemblyBinding**   |                           | Oui      |
| **détection**           |                           | Non       |
|                       | **privatePath**           | Oui      |
| **dépendance**        |                           | Non       |
| **dependentAssembly** |                           | Oui      |
| **assemblyIdentity**  |                           | Oui      |
|                       | **type**                  | Oui      |
|                       | **name**                  | Oui      |
|                       | **language**              | Non       |
|                       | **processorArchitecture** | Oui      |
|                       | **version**               | Oui      |
|                       | **publicKeyToken**        | Non       |
| **Direction**   |                           | Oui      |
|                       | **oldVersion**            | Oui      |
|                       | **newVersion**            | Oui      |



 

## <a name="file-location"></a>Emplacement du fichier

Les fichiers de configuration de l’application doivent être installés au même emplacement que le [manifeste d’application](application-manifests.md)de l’application.

## <a name="file-name-syntax"></a>Syntaxe du nom de fichier

Le nom d’un fichier de configuration d’application est le nom de l’exécutable d’application suivi de. config.

Par exemple, un fichier de configuration d’application qui fait référence à Example.exe ou Example.dll utiliserait la syntaxe de nom de fichier indiquée dans l’exemple suivant. Vous pouvez omettre le champ pour <*ID de ressource*> si vous installez le fichier de configuration en tant que fichier distinct ou si l’ID de ressource est 1.

***ID de ressource* example.exe. <# C1.config**

***ID de ressource* example.dll. <# C1.config**

## <a name="elements"></a>Éléments

Les noms des éléments et des attributs respectent la casse. Les valeurs des éléments et des attributs ne respectent pas la casse, à l’exception de la valeur de l’attribut type.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configuration

Élément conteneur pour les éléments **Windows** et **Runtime** d’un fichier de configuration d’application. Obligatoire.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

Comprend les parties du fichier de configuration de l’application qui s’appliquent à la redirection des assemblys Win32.

> [!Note]  
> L’auteur d’une application ne doit pas inclure un fichier de configuration avec un sous-élément **Windows** dans le cadre de son application. Cela peut être autorisé si le seul objectif du fichier de configuration est d’activer la fonctionnalité **privatePath** d’un élément de **détection** . L’élément de **détection** n’est pas disponible sur les systèmes antérieurs à windows Server 2008 R2 et Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Spécifie s’il faut appliquer la stratégie d’éditeur.

Cet élément a les attributs répertoriés dans le tableau suivant.



| Attribut | Description                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **appliqu** | La valeur « Yes » applique la stratégie d’éditeur. Il s'agit du paramètre par défaut. La valeur « non » n’applique pas la stratégie d’éditeur. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>runtime

Comprend les parties du fichier de configuration de l’application qui s’appliquent à la redirection des assemblys .net.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Comprend les informations de redirection pour l’application et l’assembly affecté par ce fichier de configuration de l’application. Le premier sous-élément de **assemblyBinding** doit être un **assemblyIdentity** qui identifie l’application.

À compter de Windows Server 2008 R2 et Windows 7, un élément **assemblyBinding** peut inclure un sous-élément de **détection** .

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>sonde

Sous-élément facultatif d’un élément **assemblyBinding** qui étend la recherche d’assemblys dans des répertoires supplémentaires. Les répertoires supplémentaires ne sont pas requis pour être des sous-répertoires du répertoire de l’assembly.

> [!Note]  
> Cet élément n’est pas disponible sur les systèmes antérieurs à Windows Server 2008 R2 et Windows 7 et peut uniquement être utilisé dans un élément **Windows** .

Cet élément a les attributs répertoriés dans le tableau suivant.

| Attribut       | Description                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Spécifie les [chemins d’accès relatifs](/windows/desktop/FileIO/naming-a-file) des sous-répertoires du répertoire de base de l’application qui peuvent contenir des assemblys. Neuf chemins d’accès au sous-répertoire au maximum peuvent être spécifiés. Délimitez chaque chemin d’accès de sous-répertoire par un point-virgule. |

Vous pouvez utiliser le spécificateur spécial à deux points dans un chemin d’accès pour désigner le répertoire parent du répertoire actif. Deux niveaux au-dessus du répertoire actif ne peuvent pas être spécifiés à l’aide de deux points. N’utilisez pas de triples points. Par exemple, une application qui utilise l’élément de **détection** suivant vérifie des répertoires supplémentaires pour un assembly.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Élément conteneur pour au moins un élément **dependentAssembly**. Chaque **dependentAssembly** peut se trouver dans une seule **dépendance**. Cet élément n’a pas d’attributs. Optionnel.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Le premier sous-élément doit être un élément **assemblyIdentity** qui identifie l’assembly côte à côte qui est redirigé par le fichier de configuration de l’application. Un **dependentAssembly** n’a pas d’attributs.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

En tant que premier sous-élément d’un élément **assemblyBinding** , **assemblyIdentity** décrit et identifie de façon unique une application. Le fichier de configuration de l’application redirige la liaison de cette application vers des assemblys côte à côte. Par exemple, l' **assemblyIdentity** suivant indique que le fichier de configuration de l’application affecte la liaison de l’application mysampleApp aux assemblys côte à côte. Les assemblys redirigés sont identifiés dans un **dependentAssembly**.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit un assembly côte à côte dont dépend l’application. Le fichier de configuration de l’application reconfigure l’identité de cet assembly requis. Par exemple, les conditions **assemblyIdentity** et **bindingRedirect** suivantes reconfigurent une dépendance sur Microsoft. Windows. SampleAssembly, de la version 2.0.0.0 à la version 2.1.0.0.

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

Notez que chaque **assemblyIdentity** inclus dans un **dependentAssembly** doit correspondre exactement à l' **assemblyIdentity** dans le manifeste de l' [assembly](assembly-manifests.md)de l’assembly.

L’élément **assemblyIdentity** a les attributs suivants. Il n’a pas de sous-éléments.

| Attribut                 | Description                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | La valeur doit être Win32 (en minuscules). Obligatoire.                                                                                                                                                                                                                                                                      |
| **name**                  | L’attribut Name identifie l’application affectée par le fichier de configuration de l’application ou l’assembly en cours de redirection. Utilisez le format suivant pour le nom : Organization.Division.Name. Obligatoire. Par exemple : Microsoft. Windows. MysampleApp ou Microsoft. Windows. MysampleAsm.<br/>            |
| **language**              | Identifie la langue. Optionnel. Pour un **assemblyIdentity** faisant référence à un assembly, si l’assembly est spécifique à une langue, spécifiez le code de langue DHTML. Si l’assembly est destiné à une utilisation mondiale (langue neutre), définissez la valeur sur « \* ».<br/>                                                            |
| **processorArchitecture** | Spécifie le processeur qui exécute l’application.                                                                                                                                                                                                                                                                     |
| **version**               | Spécifie la version de l’application ou de l’assembly. Utilisez la syntaxe de version en quatre parties : MMMM. nnnn. oooo. pppp. Obligatoire.                                                                                                                                                                                                   |
| **publicKeyToken**        | Pour un **assemblyIdentity** faisant référence à un assembly, une chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé. La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits. Obligatoire pour tous les assemblys côte à côte partagés. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>Direction

L’élément **bindingRedirect** contient des informations de redirection pour la liaison de l’assembly. Chaque **bindingRedirect** doit être inclus dans un **assembly** unique. La syntaxe de version en quatre parties de la nouvelle version et de l’ancienne version doit spécifier les mêmes versions majeures et mineures.

Cet élément a les attributs répertoriés dans le tableau suivant.

| Attribut      | Description                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Spécifie la version de l’assembly qui est substituée et redirigée. Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn. Spécifiez une plage de versions par un tiret sans espaces. Par exemple, 2.14.3.0 ou 2.14.3.0 2.16.0.0. Obligatoire. |
| **newVersion** | Spécifie la version de l’assembly de remplacement. Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Notes

Les fichiers de configuration de l’application ne spécifient pas de fichiers.

## <a name="example"></a>Exemple

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
