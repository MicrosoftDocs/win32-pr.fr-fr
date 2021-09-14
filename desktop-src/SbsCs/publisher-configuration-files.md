---
description: Un fichier de configuration d’éditeur est un fichier XML qui redirige globalement les applications et les assemblys de à l’aide d’une version d’un assembly côte à côte vers une autre version du même assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Publisher Fichiers de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011337"
---
# <a name="publisher-configuration-files"></a>Publisher Fichiers de configuration

Un fichier de configuration d’éditeur est un fichier XML qui redirige globalement les applications et les assemblys de à l’aide d’une version d’un assembly côte à côte vers une autre version du même assembly. En règle générale, l’éditeur de l’assembly émet une mise à jour ou un correctif de sécurité compatible pour chaque assembly en émettant un fichier de configuration d’éditeur à installer avec une mise à jour Service Pack. C’est ce que l’on appelle la configuration du serveur de [publication](publisher-configuration.md). pour plus d’informations sur ce type de [configuration](configuration.md) , consultez Publisher configuration.

Publisher fichiers de configuration possèdent les éléments et les attributs suivants. pour obtenir une liste complète du schéma XML, consultez [Publisher schéma du fichier de Configuration](publisher-configuration-file-schema.md).



| Élément               | Attributs                | Obligatoire |
|-----------------------|---------------------------|----------|
| **chargeur**          |                           | Oui      |
|                       | **manifestVersion**       | Oui      |
| **assemblyIdentity**  |                           | Oui      |
|                       | **type**                  | Oui      |
|                       | **name**                  | Oui      |
|                       | **language**              | Non       |
|                       | **processorArchitecture** | Non       |
|                       | **version**               | Oui      |
|                       | **publicKeyToken**        | Non       |
| **dépendance**        |                           | Non       |
| **dependentAssembly** |                           | Non       |
| **Direction**   |                           | Oui      |
|                       | **oldVersion**            | Oui      |
|                       | **newVersion**            | Oui      |



 

## <a name="file-location"></a>Emplacement du fichier

Publisher fichiers de configuration doivent être installés dans le dossier WinSxS. Ils sont généralement installés en tant que fichiers distincts, mais les fichiers de configuration du serveur de publication peuvent également être inclus en tant que ressource dans une DLL. Un fichier de configuration d’éditeur ne peut pas être inclus en tant que ressource dans un fichier EXE. Un fichier EXE peut inclure un [manifeste d’application](application-manifests.md) en tant que ressource.

## <a name="file-name-syntax"></a>Syntaxe du nom de fichier

Le nom de fichier d’un fichier de configuration d’éditeur possède la *stratégie* de formulaire. *majeure*. *mineure*. *AssemblyName* , où *major* et *Minor* font référence aux parties majeures et secondaires de la [version d’assembly](assembly-versions.md) qui est affectée. Le *AssemblyName* fait référence au nom de l’assembly.

Par exemple, un fichier de configuration d’éditeur pour la version 6,0 de Microsoft. Windows. L’assembly de contrôles communs porterait le nom suivant :

<dl> Policy. 6.0. Microsoft. Windows. Contrôles communs  
</dl>

N’utilisez pas de fichiers de configuration de stratégie pour incrémenter la version majeure ou mineure d’un assembly. Par exemple, ne redirigez pas la version 6.0.0.0 vers 7.0.0.0 ou 6.1.0.0. Lorsqu’une application fait référence à une version d’assembly, telle que 6.0.0.0, côte à côte vérifie la présence de fichiers de configuration de stratégie avec les versions principales et secondaires spécifiées, par exemple 6,0. L’application est ensuite redirigée vers une autre version de l’assembly, par exemple 6.0.1.0. Si un fichier de configuration d’éditeur incrémente la version majeure ou mineure d’un assembly, la redirection ultérieure de l’assembly peut nécessiter l’émission de plusieurs fichiers de configuration de stratégie.

## <a name="elements"></a>Éléments

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**chargeur**
</dt> <dd>

Élément conteneur. Son premier sous-élément doit être un **assemblyIdentity**. Obligatoire.

L’élément assembly doit se trouver dans l’espace de noms **urn : schemas-microsoft-com : ASM. v1**. Les éléments enfants de l’assembly doivent également être dans cet espace de noms, par héritage ou par balisage.

L’élément **assembly** a les attributs suivants.



| Attribut           | Description                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L’attribut **manifestVersion** doit avoir la valeur 1,0. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Décrit et identifie de façon unique un assembly côte à côte.

En tant que premier sous-élément d’un élément **assembly** , l’élément **assemblyIdentity** décrit l’assembly côte à côte dont une ou plusieurs de ses dépendances d’assembly ont été modifiées. Le fichier de configuration du serveur de publication redirige les dépendances de l’assembly identifié. Par exemple, l' **assemblyIdentity** suivant indique que le fichier de configuration du serveur de publication affecte les dépendances de Microsoft x86. Windows. Assembly 6.0.0.0 pop.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit une dépendance d’assembly côte à côte. Le fichier de configuration du serveur de publication reconfigure l’identité de cet assembly côte à côte obligatoire. La modification est spécifiée dans une **bindingRedirect**. Par exemple, l’état **assemblyIdentity** suivant modifie les dépendances de Microsoft. Windows. SampleAssembly version 2.0.0.0 à une dépendance sur Microsoft. Windows. SampleAssembly version 2.0.1.0.

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

L’élément **assemblyIdentity** a les attributs suivants. Il n’a pas de sous-éléments.



| Attribut                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Spécifie le type d’assembly. Obligatoire. Dans le champ **assemblyIdentity** de l’assembly affecté, la valeur de l’attribut **type** doit être définie sur Win32-Policy. La valeur Win32-Policy doit être en minuscules.<br/> Dans le champ **assemblyIdentity** de la dépendance de l’assembly en cours de modification, la valeur de l’attribut **type** doit être définie sur Win32. La valeur Win32 doit être en lettres minuscules.<br/>                                                                                                                                                                                                             |
| **name**                  | Nomme un assembly de manière unique. Obligatoire. Dans l’objet **assemblyIdentity** de l’assembly affecté, le nom a la *stratégie* de formulaire. *majeure*. *mineure*. *AssemblyName* , où *major* et *Minor* font référence aux parties majeures et secondaires de la version de l' [assembly](assembly-versions.md).<br/> Dans l' **assemblyIdentity** pour la dépendance de l’assembly en cours de modification, le nom se présente sous la forme Organization.Division.Name. Par exemple, Microsoft. Windows. MysampleApp.<br/>                                                                                                                                                                                 |
| **language**              | Identifie le langage de l’assembly. Optionnel. Dans l’objet **assemblyIdentity** de l’assembly affecté, si l’assembly est spécifique à une langue, spécifiez le code de langue DHTML. Si l’assembly est destiné à une utilisation dans le monde entier (langue neutre), omettez cet attribut.<br/> Dans le **assemblyIdentity** pour la dépendance de l’assembly en cours de modification, si l’assembly est spécifique à la langue, spécifiez le code de langue DHTML. Si l’assembly est destiné à une utilisation mondiale (langue neutre), définissez la valeur sur « \* ».<br/>                                                                                                                            |
| **processorArchitecture** | Spécifie le processeur qui exécute l’application.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Spécifie la version de l’assembly. Utilisez la syntaxe de version en quatre parties : MMMM. nnnn. oooo. pppp Obligatoire uniquement dans le **assemblyIdentity** du contexte def. Ne spécifiez pas l’attribut de version dans le **assemblyIdentity** du contexte de référence.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **publicKeyToken**        | Chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé. La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits. Un publicKeyToken est requis pour tous les assemblys côte à côte partagés. Le publicKeyToken utilisé pour le fichier de configuration du serveur de publication doit être la même clé que celle utilisée pour l’assembly signé. Publisher fichiers de configuration peuvent être signés à l’aide des mêmes outils que ceux utilisés avec les assemblys, consultez [exemple de signature d’assembly](assembly-signing-example.md) et [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md). |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**dépendance**
</dt> <dd>

Élément conteneur facultatif pour au moins un élément **dependentAssembly**. Elle n’a pas d’attribut.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Chaque **dependentAssembly** doit se trouver à l’intérieur d’une seule **dépendance**. Un **dependentAssembly** n’a pas d’attributs. Le premier sous-élément de **dependentAssembly** doit être un **assemblyIdentity** pour l’assembly côte à côte qui est reconfiguré par la configuration du serveur de publication.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**Direction**
</dt> <dd>

L’élément **bindingRedirect** contient des informations de redirection pour la liaison de l’assembly.

Cet élément a les attributs répertoriés dans le tableau suivant.



| Attribut      | Description                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Spécifie la version de l’assembly qui est substituée et redirigée. Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn. Spécifiez une plage de versions par un tiret sans espaces. Par exemple, 2.14.3.0 ou 2.14.3.0 2.16.0.0. Obligatoire. |
| **newVersion** | Spécifie la version de l’assembly de remplacement. Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Publisher fichiers de configuration ne spécifient pas de fichiers. Notez que les fichiers de stratégie spécifiques à une langue sont distincts du fichier de configuration du serveur de publication.

## <a name="example"></a>Exemple

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




