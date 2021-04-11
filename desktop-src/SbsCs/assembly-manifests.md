---
description: Un manifeste d’assembly est un fichier XML qui décrit un assembly côte à côte.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifestes d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254702d5044331fa5d47def815556dbd8edef2f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203387"
---
# <a name="assembly-manifests"></a>Manifestes d’assembly

Un manifeste d’assembly est un fichier XML qui décrit un assembly côte à côte. Les manifestes d’assembly décrivent les noms et les versions des assemblys, des fichiers et des ressources côte à côte de l’assembly, ainsi que la dépendance de l’assembly par d’autres assemblys côte à côte. Pour corriger l’installation, l’activation et l’exécution d’assemblys côte à côte, le manifeste de l’assembly doit toujours accompagner un assembly sur le système.

Pour obtenir une liste complète du schéma XML, consultez [schéma de fichier manifeste](manifest-file-schema.md).

Les manifestes d’assembly ont les éléments et attributs suivants.



| Élément                           | Attributs                | Obligatoire |
|-----------------------------------|---------------------------|----------|
| **assembly**                      |                           | Oui      |
|                                   | **manifestVersion**       | Oui      |
| **noinherits**                 |                           | Non       |
| **assemblyIdentity**              |                           | Oui      |
|                                   | **type**                  | Oui      |
|                                   | **name**                  | Oui      |
|                                   | **language**              | Non       |
|                                   | **processorArchitecture** | Non       |
|                                   | **version**               | Oui      |
|                                   | **publicKeyToken**        | Non       |
| **dépendance**                    |                           | Non       |
| **dependentAssembly**             |                           | Non       |
| **file**                          |                           | Non       |
|                                   | **name**                  | Oui      |
|                                   | **hashAlg**               | Non       |
|                                   | **hash**                  | Non       |
| **ComClass**                      |                           | Non       |
|                                   | **description**           | Non       |
|                                   | **identificateur**                 | Oui      |
|                                   | **threadingModel**        | Non       |
|                                   | **tlbid**                 | Non       |
|                                   | **ProgID**                | Non       |
|                                   | **miscStatus**            | Non       |
|                                   | **miscStatusIcon**        | Non       |
|                                   | **miscStatusContent**     | Non       |
|                                   | **miscStatusDocPrint**    | Non       |
|                                   | **miscStatusDocPrint**    | Non       |
| **exportation**                       |                           | Non       |
|                                   | **tlbid**                 | Oui      |
|                                   | **version**               | Oui      |
|                                   | **helpDir**               | Oui      |
|                                   | **IDRessource**            | Non       |
|                                   | **flags**                 | Non       |
| **comInterfaceExternalProxyStub** |                           | Non       |
|                                   | **vaut**                   | Oui      |
|                                   | **baseInterface**         | Non       |
|                                   | **numMethods**            | Non       |
|                                   | **name**                  | Non       |
|                                   | **tlbid**                 | Non       |
|                                   | **proxyStubClsid32**      | Non       |
| **comInterfaceProxyStub**         |                           | Non       |
|                                   | **vaut**                   | Oui      |
|                                   | **name**                  | Oui      |
|                                   | **tlbid**                 | Non       |
|                                   | **baseInterface**         | Non       |
|                                   | **numMethods**            | Non       |
|                                   | **proxyStubClsid32**      | Non       |
|                                   | **threadingModel**        | Non       |
| **windowClass**                   |                           | Non       |
|                                   | **avec version**             | Non       |



 

## <a name="file-location"></a>Emplacement du fichier

Les manifestes d’assembly peuvent être installés dans trois emplacements :

-   En tant que manifestes qui accompagnent les [assemblys partagés](/windows/desktop/Msi/shared-assemblies), les manifestes d’assembly doivent être installés en tant que fichier distinct dans le cache d’assembly côte à côte. Il s’agit généralement du dossier WinSxS dans le répertoire Windows.
-   Comme les manifestes qui accompagnent les [assemblys privés](/windows/desktop/Msi/private-assemblies), les manifestes d’assembly doivent être installés dans la structure de répertoires de l’application. Il s’agit généralement d’un fichier distinct dans le même dossier que le fichier exécutable de l’application.
-   En tant que ressource dans une DLL, l’assembly est disponible pour l’utilisation privée de la DLL. Un manifeste d’assembly ne peut pas être inclus en tant que ressource dans un fichier EXE. Un fichier EXE peut inclure un [manifeste d’application](application-manifests.md) en tant que ressource.

## <a name="file-name-syntax"></a>Syntaxe du nom de fichier

Le nom d’un manifeste d’assembly est un nom de fichier valide suivi de. manifest.

Par exemple, un manifeste d’assembly qui fait référence à myAssembly utilise la syntaxe de nom de fichier suivante. Vous pouvez omettre le champ *ID de ressource* <> si le manifeste de l’assembly est installé en tant que fichier distinct ou si l’ID de ressource est 1.

<dl> myAssembly. <resource ID> . du
</dl>

> [!Note]  
> En raison de la façon dont les recherches côte à côte pour les assemblys privés sont effectuées, les restrictions d’affectation de noms suivantes s’appliquent lors de l’empaquetage d’une DLL en tant qu’assembly privé. Une méthode recommandée consiste à placer le manifeste d’assembly dans la DLL en tant que ressource. Dans ce cas, l’ID de ressource doit être égal à 1 et le nom de l’assembly privé peut être le même que le nom de la DLL. Par exemple, si le nom de la DLL est Microsoft.Windows.mysample.dll, la valeur de l’attribut Name utilisé dans l’élément **assemblyIdentity** du manifeste peut également être Microsoft. Windows. MySample. Une autre méthode consiste à placer le manifeste de l’assembly dans un fichier séparé. Dans ce cas, le nom de l’assembly et son manifeste doivent être différents du nom de la DLL. Par exemple, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest et Microsoft.Windows.Mysample.dll. Pour plus d’informations sur la façon dont les recherches côte à côte pour les assemblys privés, consultez [séquence de recherche](assembly-searching-sequence.md)d’assemblys.

 

## <a name="elements"></a>Éléments

Les noms des éléments et des attributs respectent la casse. Les valeurs des éléments et des attributs ne respectent pas la casse, à l’exception de la valeur de l’attribut type.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**chargeur**
</dt> <dd>

Élément conteneur. Son premier sous-élément doit être un élément **assemblyIdentity** ou **NoInherit** . Le manifeste d’assembly décrit de façon unique l’assembly côte à côte identifié par l' **assemblyIdentity**. Obligatoire.

L’élément assembly doit figurer dans l’espace de noms « urn : schemas-microsoft-com : ASM. v1 ». Les éléments enfants de l’assembly doivent également être dans cet espace de noms, par héritage ou par balisage.

L’élément **assembly** a l’attribut suivant.



| Attribut           | Description                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L’attribut **manifestVersion** doit avoir la valeur 1,0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noinherits**
</dt> <dd>

Incluez cet élément dans un manifeste d’assembly pour indiquer que l’assembly gère les [contextes d’activation](activation-contexts.md) et ses objets. L’élément **noInheritable** doit être un sous-élément d’un élément **assembly** . L’élément **assemblyIdentity** doit venir après tout élément **noInheritable** . L’élément **noInheritable** est requis dans le manifeste de l’assembly si l’assembly est utilisé par les [manifestes d’application](application-manifests.md) qui incluent l’élément **noinherits** . Un élément **noInheritable** dans un manifeste d’application n’a aucun effet. Un élément **noInheritable** n’a pas d’éléments enfants.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Décrit et identifie de façon unique un assembly côte à côte.

En tant que premier sous-élément d’un élément **assembly** , **assemblyIdentity** décrit et identifie de façon unique l’assembly côte à côte qui possède ce manifeste d’assembly. C’est ce que l’on appelle le **assemblyIdentity** du contexte de définition du manifeste de l’assembly.

En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit et identifie de façon unique un assembly côte à côte utilisé par le **assemblyIdentity** du contexte def. C’est ce que l’on appelle un **assemblyIdentity** de contexte ref du manifeste de l’assembly. L’assembly DEF-Context requiert que l’assembly de contexte de référence fonctionne correctement. Notez que chaque **assemblyIdentity** du contexte de référence doit correspondre exactement à un **ASSEMBLYIDENTITY** de contexte def correspondant dans le manifeste d’assembly de l’assembly référencé.

Cet élément n’a pas de sous-éléments. L’élément **assemblyIdentity** a les attributs suivants.



| Attribut                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Spécifie le type d’assembly. La valeur doit être Win32 et en minuscules. Obligatoire.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Nomme l’assembly de manière unique. Utilisez le format suivant pour le nom de l’assembly : Organization.Division.Name. Par exemple, Microsoft. Windows. mysampleAsm. Obligatoire. Notez que, dans le cas d’une DLL empaquetée comme un assembly privé avec un fichier manifeste distinct, le nom de l’assembly doit être différent du nom de la DLL et du manifeste.<br/>                                                                              |
| **language**              | Identifie le langage de l’assembly. Optionnel. Si l’assembly est spécifique à une langue, spécifiez le code de langue DHTML. Dans le **champ de définition de contexte de** fichier (...) d’un manifeste d’assembly destiné à une utilisation mondiale (indépendant de la langue), omettez l’attribut de langue.<br/> Dans un **assemblyIdentity** de contexte de référence d’un manifeste d’assembly destiné à une utilisation dans le monde entier (indépendant de la langue), définissez la valeur de Language sur « \* ».<br/> |
| **processorArchitecture** | Spécifie le processeur. Les valeurs valides sont x86 pour Windows 32 bits et IA64 pour Windows 64 bits. Optionnel.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Spécifie la version de l’assembly. Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp. Chacun des composants séparés par des points peut être de 0-65535 inclus. Pour plus d’informations, consultez [versions d’assembly](assembly-versions.md). Obligatoire.                                                                                                                                                                                               |
| **publicKeyToken**        | Chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé. La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits. Requis pour les assemblys côte à côte partagés.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**dépendance**
</dt> <dd>

Élément conteneur incluant au moins un **dependentAssembly**. Le premier sous-élément doit être un élément **dependentAssembly** . Une **dépendance** n’a pas d’attributs. Optionnel.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Le premier sous-élément doit être un élément **assemblyIdentity** qui décrit et identifie de façon unique un assembly côte à côte qui est utilisé par l’assembly côte à côte qui possède ce manifeste d’assembly. Chaque **dependentAssembly** doit se trouver à l’intérieur d’une seule **dépendance**. Optionnel.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**txt**
</dt> <dd>

Contient les fichiers utilisés par un assembly côte à côte. Contient des sous-éléments **ComClass**, **TypeLib**, **WindowClass**, **comInterfaceProxyStub** . Optionnel.

L’élément **file** a les attributs suivants.



| Attribut   | Description                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nom du fichier, par exemple, Conctl32.dll.                                                            |
| **hashAlg** | Algorithme utilisé pour créer un hachage du fichier. Cette valeur doit être SHA1.                                 |
| **hash**    | Hachage du fichier référencé par nom. Chaîne hexadécimale de longueur selon l’algorithme de hachage. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**ComClass**
</dt> <dd>

Sous-élément d’un élément **file** . Optionnel.

L’élément **ComClass** a les attributs suivants.



| Attribut               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Nom de la classe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **identificateur**               | GUID qui identifie de façon unique la classe. Obligatoire. La valeur doit être au format d’un GUID valide.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | Modèle de thread utilisé par les classes COM in-process. Si cette propriété a la valeur null, aucun modèle de thread n’est utilisé. Le composant est créé sur le thread principal du client et les appels d’autres threads sont marshalés vers ce thread. Optionnel. Les valeurs valides sont : « Apartment », « Free », « both » et « Neutral ».                                                                                                                                                                                                                         |
| **tlbid**               | GUID de la bibliothèque de types pour ce composant COM. La valeur doit être au format d’un GUID. Optionnel.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **ProgID**              | Identificateur programmatique dépendant de la version associé au composant COM. Le format d’un ProgID est <*fournisseur*>. <*composant*>. <*version*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Les doublons dans le manifeste de l’assembly sont les informations fournies par la clé de Registre MiscStatus. Si les valeurs des attributs **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** ou **miscStatusThumbnail** sont introuvables, la valeur par défaut correspondante répertoriée dans **MiscStatus** est utilisée pour les attributs manquants. La valeur peut être une liste délimitée par des virgules des valeurs d’attribut du tableau ci-dessous. Vous pouvez utiliser cet attribut si la classe COM est une classe OCX qui requiert des valeurs de clé de Registre MiscStatus. |
| **miscStatusIcon**      | Les doublons dans le manifeste de l’assembly sont les informations fournies par l' \_ icône DVASPECT. Il peut fournir une icône d’un objet. La valeur peut être une liste délimitée par des virgules des valeurs d’attribut du tableau ci-dessous. Vous pouvez utiliser cet attribut si la classe COM est une classe OCX qui requiert des valeurs de clé de Registre MiscStatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Les doublons dans le manifeste de l’assembly sont les informations fournies par le \_ contenu DVASPECT. Il peut fournir un document composé affichable pour un écran ou une imprimante. La valeur peut être une liste délimitée par des virgules des valeurs d’attribut du tableau ci-dessous. Vous pouvez utiliser cet attribut si la classe COM est une classe OCX qui requiert des valeurs de clé de Registre MiscStatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Les doublons dans le manifeste de l’assembly sont les informations fournies par DVASPECT \_ DOCPRINT. Il peut fournir une représentation d’objet affichable sur l’écran comme s’il était imprimé sur une imprimante. La valeur peut être une liste délimitée par des virgules des valeurs d’attribut du tableau ci-dessous. Vous pouvez utiliser cet attribut si la classe COM est une classe OCX qui requiert des valeurs de clé de Registre MiscStatus.                                                                                                                                               |
| **miscStatusThumbnail** | Les doublons dans un manifeste d’assembly sont les informations fournies par la miniature de DVASPECT \_ . Il peut fournir une miniature d’un objet affichable dans un outil de navigation. La valeur peut être une liste délimitée par des virgules des valeurs d’attribut du tableau ci-dessous. Vous pouvez utiliser cet attribut si la classe COM est une classe OCX qui requiert des valeurs de clé de Registre MiscStatus.                                                                                                                                                                         |



 

L’élément **ComClass** peut avoir des éléments <progid>...</progid> comme enfants, qui répertorient les ProgID dépendants de la version.

L’exemple suivant montre un élément **ComClass** inclus dans un élément **file** .

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

Si votre classe COM est une classe OCX qui exige que la sous-clé de Registre MiscStatus spécifie comment créer et afficher un objet, vous pouvez activer l’objet en dupliquant ces informations dans le manifeste de l’assembly. Spécifiez les caractéristiques de l’objet à l’aide des attributs **MiscStatus**, **miscStatusIcon**, **miscStatusContent**, **MiscStatusDocprint** et **miscStatusThumbnail** de l’élément **ComClass** . Définissez ces attributs sur une liste séparée par des virgules de valeurs d’attribut à partir du tableau suivant. Ces attributs dupliquent les informations qui seraient fournies par une énumération DVASPECT. Si aucune valeur n’est trouvée pour **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** ou **miscStatusThumbnail**, les valeurs par défaut spécifiées dans **MiscStatus** sont utilisées. Utilisez les valeurs d’attribut du tableau suivant. Celles-ci correspondent aux indicateurs binaires d’une énumération [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) .



| Valeur d'attribut              | OLEMISC constante)                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ statique                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| insideout                    | OLEMISC \_ insideout                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | OLEMISC \_ RENDERINGISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| alignement                    | OLEMISC \_ alignement                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| ImeMode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTSMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**exportation**
</dt> <dd>

Sous-élément d’un élément **file** . Optionnel.

L’élément **TypeLib** a les attributs indiqués dans le tableau suivant.



| Attribut      | Description                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | ID unique de la bibliothèque de types. Obligatoire.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Numéro de version en deux parties de la bibliothèque de types. Si seul le numéro de version mineure augmente, toutes les fonctionnalités de la bibliothèque de types précédente sont prises en charge de manière compatible. Si le numéro de version principale change, le code qui a été compilé avec la bibliothèque de types doit être recompilé. Le numéro de version de la bibliothèque de types peut différer du numéro de version de l’application. Obligatoire.                                      |
| **helpDir**    | Répertoire où se trouve le fichier d’aide pour les types de la bibliothèque de types. Si l’application prend en charge les bibliothèques de types pour plusieurs langues, les bibliothèques peuvent faire référence à des noms de fichiers différents dans le répertoire du fichier d’aide. Si aucune valeur n’est spécifiée, spécifiez «». Obligatoire.                                                                                                                                                          |
| **IDRessource** | Représentation sous forme de chaîne hexadécimale de l’identificateur de paramètres régionaux (LCID). Il s’agit d’un à quatre chiffres hexadécimaux sans préfixe 0x et sans zéro non significatif. Le LCID peut avoir un identificateur de sous-langue neutre. Pour plus d’informations, consultez [identificateurs de paramètres régionaux](/windows/desktop/Intl/locale-identifiers). Optionnel.                                                                                                                                      |
| **flags**      | Représentation sous forme de chaîne des indicateurs de la bibliothèque de types pour cette bibliothèque de types. En particulier, il doit s’agir de « RESTRICTED », « CONTROL », « HIDDEN » et « HASDISKIMAGE ». Il s’agit des valeurs de l’énumération [**LIBflags**](/windows/win32/api/oaidl/ne-oaidl-libflags) , qui sont les mêmes que celles spécifiées dans le paramètre *uLibFlags* de la méthode [**ICreateTypeLib :: SetLibFlags**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) . Optionnel. |



 

L’exemple suivant montre un élément **TypeLib** inclus dans un élément **file** .

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** est un sous-élément d’un élément **assembly** et est utilisé pour les interfaces d’automatisation. Par exemple, [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et ses interfaces dérivées. Optionnel.

L’implémentation par défaut du stub proxy est appropriée pour la plupart des interfaces d’automatisation, telles que les interfaces dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Le stub de proxy d’interface et toutes les autres implémentations externes de l’interface proxy-stub doivent être listés dans **comInterfaceExternalProxyStub**. L’élément **comInterfaceExternalProxyStub** a les attributs indiqués dans le tableau suivant.



| Attribut         | Description                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **vaut**           | IID de l’interface pour laquelle le proxy est déclaré. Obligatoire. La valeur doit se présenter sous la forme : « {iid} ».                                                                         |
| **baseInterface** | IID de l’interface à partir de laquelle l’attribut décrit par l’attribut **IID** est dérivé. Cet attribut est facultatif. La valeur doit se présenter sous la forme : « {iid} ».                            |
| **numMethods**    | Nombre de méthodes implémentées par l’interface. Cet attribut est facultatif. La valeur doit être au format : "n".                                                                       |
| **name**          | Nom de l’interface tel qu’il apparaîtrait dans le code. Par exemple, « IViewObject ». Il ne doit pas s’agir d’une chaîne descriptive. Cet attribut est facultatif. La valeur doit être au format : « Name ». |
| **tlbid**         | Bibliothèque de types qui contient la description de l’interface spécifiée par l’attribut **IID** . Cet attribut est facultatif. La valeur doit se présenter sous la forme : « {TLBID (} ».                |
| proxyStubClsid32  | Mappe un IID à un CLSID dans des dll de proxy 32 bits.                                                                                                                                                |



 

L’exemple suivant montre un élément **comInterfaceExternalProxyStub** .

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

Sous-élément d’un élément **file** . Optionnel.

Si un fichier de l’assembly implémente un stub proxy, la balise file correspondante doit inclure un sous-élément **comInterfaceProxyStub** ayant des attributs qui sont identiques à un élément **comInterfaceProxyStub** . Le marshaling des interfaces entre les processus et les threads peut ne pas fonctionner comme prévu si vous omettez certaines des dépendances **comInterfaceProxyStub** pour votre composant.

L’élément **comInterfaceProxyStub** a les attributs suivants.



| Attribut            | Description                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **vaut**              | La. IID de l’interface pour laquelle le proxy est déclaré. Obligatoire. La valeur doit se présenter sous la forme : « {iid} ».                                                                                                                                                                                        |
| **name**             | Nom de l’interface tel qu’il apparaîtrait dans le code. Par exemple, « IViewObject ». Il ne doit pas s’agir d’une chaîne descriptive. Cet attribut est facultatif. La valeur doit être au format : « Name ».                                                                                                                 |
| **tlbid**            | Bibliothèque de types qui contient la description de l’interface spécifiée par l’attribut **IID** . Cet attribut est facultatif. La valeur doit se présenter sous la forme : « {TLBID (} ».                                                                                                                                 |
| **baseInterface**    | IID de l’interface à partir de laquelle l’attribut décrit par l’attribut **IID** est dérivé. Cet attribut est facultatif. La valeur doit se présenter sous la forme : « {iid} ».                                                                                                                                            |
| **numMethods**       | Nombre de méthodes implémentées par l’interface. Cet attribut est facultatif. La valeur doit être au format : "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Mappe un IID à un CLSID dans des dll de proxy 32 bits.                                                                                                                                                                                                                                                                |
| **threadingModel**   | Modèle de thread utilisé par les classes COM in-process. Si cette propriété a la valeur null, aucun modèle de thread n’est utilisé. Le composant est créé sur le thread principal du client et les appels d’autres threads sont marshalés vers ce thread. Optionnel. Les valeurs valides sont : « Apartment », « Free », « both » et « Neutral ». |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

Nom d’une classe Windows dont la version doit être gérée. L’élément **WindowClass** a l’attribut suivant.



| Attribut     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **avec version** | Cet attribut détermine si le nom de classe de fenêtre interne utilisé dans l’inscription contient la version de l’assembly contenant la classe de fenêtre. La valeur de cet attribut peut être « oui » ou « non ». La valeur par défaut est « oui ». La valeur « non » ne doit être utilisée que si la même classe de fenêtre est définie par un composant côte à côte et un composant équivalent non côte à côte et que vous souhaitez les traiter comme la même classe de fenêtre. Notez que les règles habituelles relatives à l’inscription de la classe de fenêtre s’appliquent uniquement le premier composant qui inscrit la classe de fenêtre sera en mesure de l’inscrire dans la mesure où sa version n’est pas gérée. |



 

L’exemple suivant montre un élément **WindowClass** inclus dans un élément **file** .

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Exemple

Voici un exemple de manifeste d’assembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

