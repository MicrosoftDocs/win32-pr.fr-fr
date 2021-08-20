---
description: Un manifeste d'application est un fichier XML qui décrit et identifie les assemblys côte à côte partagés et privés auxquels une application doit se lier au moment de l'exécution.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestes d’application
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: a1ced7ffb4052f418e989e907f26abb85c2c63db
ms.sourcegitcommit: 25211012b002a7d1303e438277373d7faf958a68
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122436707"
---
# <a name="application-manifests"></a>Manifestes d’application

Un manifeste d'application est un fichier XML qui décrit et identifie les assemblys côte à côte partagés et privés auxquels une application doit se lier au moment de l'exécution. Il doit s'agir des mêmes versions d'assembly qui ont été utilisées pour tester l'application. Les manifestes d'application peuvent également décrire les métadonnées de fichiers privés pour l'application.

Pour obtenir une liste complète du schéma XML, consultez [schéma de fichier manifeste](manifest-file-schema.md).

Les manifestes d’application comportent les éléments et les attributs suivants.

| Élément                               | Attributs                | Obligatoire |
|---------------------------------------|---------------------------|----------|
| **chargeur**                          |                           | Oui      |
|                                       | **manifestVersion**       | Oui      |
| **noInherit**                         |                           | Non       |
| **assemblyIdentity**                  |                           | Oui      |
|                                       | **type**                  | Oui      |
|                                       | **name**                  | Oui      |
|                                       | **language**              | Non       |
|                                       | **processorArchitecture** | Non       |
|                                       | **version**               | Oui      |
|                                       | **publicKeyToken**        | Non       |
| **compatibilité**                     |                           | Non       |
| **application**                       |                           | Non       |
| **pris en charge**                       | **Id**                    | Non       |
| **maxversiontested**                  | **Id**                    | Non       |
| **dépendance**                        |                           | Non       |
| **dependentAssembly**                 |                           | Non       |
| **file**                              |                           | Non       |
|                                       | **name**                  | Non       |
|                                       | **hashAlg**               | Non       |
|                                       | **hash**                  | Non       |
| **activeCodePage**                    |                           | Non       |
| **Élever**                       |                           | Non       |
| **disableTheming**                    |                           | Non       |
| **disableWindowFiltering**            |                           | Non       |
| **dpiAware**                          |                           | Non       |
| **dpiAwareness**                      |                           | Non       |
| **gdiScaling**                        |                           | Non       |
| **highResolutionScrollingAware**      |                           | Non       |
| **longPathAware**                     |                           | Non       |
| **printerDriverIsolation**            |                           | Non       |
| **ultraHighResolutionScrollingAware** |                           | Non       |
| **msix**                              |                           | Non       |
| **heapType**                          |                           | Non       |

## <a name="file-location"></a>Emplacement du fichier

Les manifestes d’application doivent être inclus en tant que ressource dans le fichier EXE ou la DLL de l’application.

Pour plus d’informations, consultez [installation d’assemblys côte à côte](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Syntaxe du nom de fichier

Le nom d’un fichier manifeste d’application est le nom de l’exécutable de l’application suivi de. manifest.

Par exemple, un manifeste d’application qui fait référence à example.exe ou example.dll utiliserait la syntaxe de nom de fichier suivante. Vous pouvez omettre le champ *ID de ressource* <> si l’ID de ressource est 1.

***ID de ressource* example.exe. <>. manifest**

***ID de ressource* example.dll. <>. manifest**

## <a name="elements"></a>Éléments

Les noms des éléments et des attributs respectent la casse. Les valeurs des éléments et des attributs ne respectent pas la casse, à l’exception de la valeur de l’attribut type.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>assembly

Élément conteneur. Son premier sous-élément doit être un élément **NoInherit** ou **assemblyIdentity** . Obligatoire.

L’élément **assembly** doit figurer dans l’espace de noms « urn : schemas-microsoft-com : ASM. v1 ». Les éléments enfants de l’assembly doivent également être dans cet espace de noms, par héritage ou par balisage.

L’élément **assembly** a les attributs suivants.



| Attribut           | Description                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | L’attribut **manifestVersion** doit avoir la valeur 1,0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Incluez cet élément dans un manifeste d’application pour définir les [contextes d’activation](activation-contexts.md) générés à partir du manifeste avec l’indicateur « no Inherit ». Lorsque cet indicateur n’est pas défini dans un contexte d’activation et que le contexte d’activation est actif, il est hérité par les nouveaux threads dans les mêmes processus, fenêtres, procédures de fenêtre et [appels de procédure asynchrone](/windows/desktop/Sync/asynchronous-procedure-calls). La définition de cet indicateur empêche le nouvel objet d’hériter du contexte actif.

L’élément **NoInherit** est facultatif et généralement omis. La plupart des assemblys ne fonctionnent pas correctement à l’aide d’un contexte d’activation sans héritage, car l’assembly doit être conçu explicitement pour gérer la propagation de son propre contexte d’activation. L’utilisation de l’élément **NoInherit** requiert que tous les assemblys dépendants référencés par le manifeste d’application aient un élément **noinherits** dans leur [manifeste d’assembly](assembly-manifests.md).

Si **NoInherit** est utilisé dans un manifeste, il doit s’agir du premier sous-élément de l’élément **assembly** . L’élément **assemblyIdentity** doit être placé immédiatement après l’élément **NoInherit** . Si **NoInherit** n’est pas utilisé, **assemblyIdentity** doit être le premier sous-élément de l’élément **assembly** . L’élément **NoInherit** n’a pas d’éléments enfants. Il ne s’agit pas d’un élément valide dans les [manifestes d’assembly](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

En tant que premier sous-élément d’un élément **assembly** , **assemblyIdentity** décrit et identifie de façon unique l’application qui possède ce manifeste d’application. En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit un assembly côte à côte requis par l’application. Notez que chaque assembly référencé dans le manifeste de l’application nécessite un **assemblyIdentity** qui correspond exactement à l’expression **assemblyIdentity** dans le manifeste de l’assembly de l’assembly référencé.

L’élément **assemblyIdentity** a les attributs suivants. Il n’a pas de sous-éléments.

| Attribut                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Spécifie l’application ou le type d’assembly. La valeur doit être Win32 et tout en minuscules. Obligatoire.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Nomme l’application ou l’assembly de manière unique. Utilisez le format suivant pour le nom : Organization.Division.Name. Par exemple, Microsoft. Windows. mysampleApp. Obligatoire.                                                                                                                                                                                                                                                               |
| **language**              | Identifie la langue de l’application ou de l’assembly. facultatif. Si l’application ou l’assembly est spécifique à une langue, spécifiez le code de langue DHTML. Dans le champ **assemblyIdentity** d’une application destinée à une utilisation mondiale (indépendant de la langue), omettez l’attribut Language.<br/> Dans un **assemblyIdentity** d’un assembly destiné à une utilisation dans le monde entier (indépendant de la langue), définissez la valeur de Language sur « \* ».<br/> |
| **processorArchitecture** | Spécifie le processeur. Les valeurs autorisées sont `x86`, `amd64`, `arm` et `arm64`. facultatif.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Spécifie la version de l’application ou de l’assembly. Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp. Chacun des composants séparés par des points peut être de 0-65535 inclus. Pour plus d’informations, consultez [versions d’assembly](assembly-versions.md). Obligatoire.                                                                                                                                                                        |
| **publicKeyToken**        | Chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’application ou l’assembly est signé. La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits. Obligatoire pour tous les assemblys côte à côte partagés.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilité

Contient au moins une **application**. Elle n’a pas d’attribut. facultatif. les manifestes d’Application sans élément de compatibilité ont par défaut la compatibilité Windows Vista sur Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Contient au moins un élémentos **pris en charge** . à partir de Windows 10, la version 1903 peut également contenir un élément **maxversiontested** facultatif. Elle n’a pas d’attribut. facultatif.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>pris en charge

L’élément **pris en charge** a l’attribut suivant. Il n’a pas de sous-éléments.

| Attribut | Description   |
|-----------|-----------------------|
| **Id**    | Affectez à l’attribut ID la valeur **{e2011457-1546-43C5-a5fe-008deee3d3f0}** pour exécuter l’application à l’aide de la fonctionnalité Vista. cela peut permettre à une application conçue pour Windows Vista de s’exécuter sur un système d’exploitation ultérieur. <br/> affectez à l’attribut Id la valeur **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** pour exécuter l’application à l’aide de la fonctionnalité Windows 7.<br/> les Applications qui prennent en charge Windows fonctionnalités Vista, Windows 7 et Windows 8 ne nécessitent pas de manifestes séparés. dans ce cas, ajoutez les guid pour tous les systèmes d’exploitation Windows.<br/> pour plus d’informations sur le comportement de l’attribut **Id** dans Windows, consultez le guide de [compatibilité Windows 8 et Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Les GUID suivants correspondent aux systèmes d’exploitation indiqués :<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 et Windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 et Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 et Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 et Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista et Windows Server 2008<br/> vous pouvez tester cela sur Windows 7 ou Windows 8. x en exécutant moniteur de ressource (resmon), en accédant à l’onglet uc, en cliquant avec le bouton droit sur les étiquettes de colonne, « sélectionner une colonne... » et en cochant « contexte du système d’exploitation ». sur Windows 8. x, vous trouverez également cette colonne disponible dans le gestionnaire des tâches (taskmgr). le contenu de la colonne indique la valeur la plus élevée trouvée ou « Windows Vista » comme valeur par défaut. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

l’élément **maxversiontested** spécifie les versions de Windows pour lesquelles l’application a été testée à partir de la version minimale du système d’exploitation que l’application prend en charge jusqu’à la version maximale. L’ensemble complet des versions est disponible [ici](https://developer.microsoft.com/windows/downloads/sdk-archive/). Elle est destinée à être utilisée par les applications de bureau qui utilisent des [îlots XAML](/windows/apps/desktop/modernize/xaml-islands) et qui ne sont pas déployées dans un package MSIX. cet élément est pris en charge dans Windows 10, la version 1903 et les versions ultérieures.

L’élément **maxversiontested** a l’attribut suivant. Il n’a pas de sous-éléments.

| Attribut | Description    |
|-----------|----------------|
| **Id**    | définissez l’attribut Id sur une chaîne de version en 4 parties qui spécifie la version maximale de Windows pour laquelle l’application a été testée. Par exemple, « 10.0.18226.0 ». |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Contient au moins un **dependentAssembly**. Elle n’a pas d’attribut. facultatif.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Le premier sous-élément de **dependentAssembly** doit être un élément **assemblyIdentity** qui décrit un assembly côte à côte requis par l’application. Chaque **dependentAssembly** doit se trouver à l’intérieur d’une seule **dépendance**. Elle n’a pas d’attribut.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>fichier

Spécifie les fichiers qui sont privés pour l’application. facultatif.

L’élément **file** a les attributs indiqués dans le tableau suivant.



| Attribut   | Description                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nom du fichier. Par exemple, Comctl32.dll.                                                            |
| **hashAlg** | Algorithme utilisé pour créer un hachage du fichier. Cette valeur doit être SHA1.                                 |
| **hash**    | Hachage du fichier référencé par nom. Chaîne hexadécimale de longueur selon l’algorithme de hachage. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

sur Windows 10, cet élément force un processus à utiliser UTF-8 comme page de code de processus. Pour plus d’informations, consultez [utiliser la page de codes UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page). sur Windows 10, la seule valeur valide pour **activeCodePage** est **UTF-8**.

à partir de Windows 11, cet élément permet également de sélectionner la page de codes héritée non UTF-8 ou les pages de codes pour des paramètres régionaux spécifiques pour la compatibilité des applications héritées. Les applications modernes sont vivement encouragées à utiliser Unicode. sur Windows 11, **activeCodePage** peut également être défini sur la valeur **Legacy** ou sur un nom de paramètres régionaux comme en **-US** ou **ja-JP**.

- Sur les machines configurées sur une page de codes active du système UTF-8, l' **héritage** rétablira les pages de codes des paramètres régionaux système. si les paramètres régionaux du système n’ont pas de pages de codes définies, Windows-1252/437 sera utilisé. le paramètre de page de codes **hérité** est pris en charge uniquement dans les manifestes de Fusion et à partir de Windows 11 uniquement.
- Lorsqu’un nom de paramètres régionaux, tel que en **-US** , est fourni, la page de codes de processus est définie correctement pour cette page de codes de paramètres régionaux. par exemple, Windows-1252 et 437 pour fr-fr, ou 932 pour ja-JP.

cet élément a été ajouté pour la première fois dans Windows 10 version 1903 (mai 2019 mise à jour). vous pouvez déclarer cette propriété et la cible/exécuter sur des builds de Windows antérieures, mais vous devez gérer la détection et la conversion de pages de codes héritées comme d’habitude. Cet élément n’a pas d’attributs. 

L’exemple suivant montre comment utiliser cet élément pour forcer le processus actuel à utiliser UTF-8 comme page de codes de processus.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>Élever

Spécifie si l’élévation automatique est activée. La **valeur true** indique qu’elle est activée. Elle n’a pas d’attribut.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Spécifie si les éléments d’interface utilisateur d’un thème sont désactivés. **True** indique que l’activation est désactivée. Elle n’a pas d’attribut.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Spécifie s’il faut désactiver le filtrage de fenêtre. **True** désactive le filtrage de fenêtre pour vous permettre d’énumérer les fenêtres immersives à partir du bureau. **disableWindowFiltering** a été ajouté dans Windows 8 et n’a pas d’attributs.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>dpiAware

Spécifie si le processus actuel prend en charge la résolution en points par pouce (dpi).

**Windows 10, version 1607 :** L’élément **dpiAware** est ignoré si l’élément **dpiAwareness** est présent. vous pouvez inclure les deux éléments dans un manifeste si vous souhaitez spécifier un comportement différent pour Windows 10, version 1607, par rapport à une version antérieure du système d’exploitation.

Le tableau suivant décrit le comportement qui se produit en fonction de la présence de l’élément **dpiAware** et du texte qu’il contient. Le texte contenu dans l’élément n’est pas sensible à la casse.

| État de l’élément **dpiAware** | Description     |
|-----------------------------------|---------|
| Absent                            | Le processus actuel ne prend pas en charge DPI par défaut. Vous pouvez modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .                                                                                                                                                            |
| Contient « true »                   | Le processus actuel prend en charge la résolution du système.                                                                                                                                                                                                                                                                                                                                                          |
| Contient « false »                  | **Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.<br/> **Windows 8.1 et Windows 10 :** le processus actuel ne prend pas en charge dpi, et vous ne pouvez pas modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |
| Contient « true/PM »                | **Windows Vista, Windows 7 et Windows 8 :** Le processus actuel prend en charge la résolution du système.<br/> **Windows 8.1 et Windows 10 :** le processus actuel prend en charge la résolution par moniteur.<br/>                                                                                                                                                                                                          |
| Contient « par moniteur »            | **Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.<br/> **Windows 8.1 et Windows 10 :** le processus actuel prend en charge la résolution par moniteur.<br/>                                                                                                                                                                                      |
| Contient une autre chaîne         | **Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.<br/> **Windows 8.1 et Windows 10 :** le processus actuel ne prend pas en charge dpi, et vous ne pouvez pas modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |

Pour plus d’informations sur les paramètres de reconnaissance dpi, consultez [comparaison des niveaux de détection PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

**dpiAware** n’a pas d’attributs.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>dpiAwareness

Spécifie si le processus actuel prend en charge la résolution en points par pouce (dpi).

la version minimale du système d’exploitation qui prend en charge l’élément **dpiAwareness** est Windows 10, version 1607. Pour les versions qui prennent en charge l’élément **dpiAwareness** , **dpiAwareness** remplace l’élément **dpiAware** . vous pouvez inclure les deux éléments dans un manifeste si vous souhaitez spécifier un comportement différent pour Windows 10, version 1607, par rapport à une version antérieure du système d’exploitation.

L’élément **dpiAwareness** peut contenir un seul élément ou une liste d’éléments séparés par des virgules. Dans ce dernier cas, le premier élément (le plus à gauche) dans la liste reconnue par le système d’exploitation est utilisé. de cette façon, vous pouvez spécifier des comportements différents pris en charge dans les versions ultérieures du système d’exploitation Windows.

Le tableau suivant décrit le comportement qui se produit en fonction de la présence de l’élément **dpiAwareness** et du texte qu’il contient dans son élément reconnu le plus à gauche. Le texte contenu dans l’élément n’est pas sensible à la casse.

| État de l’élément **dpiAwareness** :        | Description                          |
|-----------------------------------------|-------------------------------------------|
| L’élément est absent                       | L’élément **dpiAware** spécifie si le processus prend en charge dpi.                                                                                                                                                                   |
| Ne contient aucun élément reconnu            | Le processus actuel ne prend pas en charge DPI par défaut. Vous pouvez modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) . |
| Le premier élément reconnu est « système »       | Le processus actuel prend en charge la résolution du système.                                                                                                                                                                                               |
| Le premier élément reconnu est « permonitor »   | Le processus actuel prend en charge la résolution par moniteur.                                                                                                                                                                                          |
| Le premier élément reconnu est « permonitorv2 » | Le processus en cours utilise le contexte de détection par moniteur-v2 PPP. cet élément sera uniquement reconnu sur Windows 10 version 1703 ou ultérieure.                                                                                              |
| Le premier élément reconnu est « non pris en charge »      | Le processus actuel ne prend pas en charge dpi. Vous **ne pouvez pas** modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .      |

Pour plus d’informations sur les paramètres de reconnaissance dpi pris en charge par cet élément, consultez prise en charge des [dpi \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness) et du [ \_ \_ contexte de détection dpi](/windows/desktop/hidpi/dpi-awareness-context).

**dpiAwareness** n’a pas d’attributs.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

Spécifie si la mise à l’échelle GDI est activée. la version minimale du système d’exploitation qui prend en charge l’élément **gdiScaling** est Windows 10 la version 1703.

L’infrastructure GDI (Graphics Device Interface) peut appliquer la mise à l’échelle DPI aux primitives et au texte en fonction de chaque moniteur sans mettre à jour l’application elle-même. Cela peut être utile pour les applications GDI qui ne sont plus mises à jour activement.

Les graphiques non vectoriels (tels que les bitmaps, les icônes ou les barres d’outils) ne peuvent pas être mis à l’échelle par cet élément. En outre, les graphiques et le texte figurant dans les bitmaps construits dynamiquement par les applications ne peuvent pas non plus être mis à l’échelle par cet élément.

**True** indique que cet élément est activé. Elle n’a pas d’attribut.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

Spécifie si la prise en charge du défilement haute résolution est activée. La **valeur true** indique qu’elle est activée. Elle n’a pas d’attribut.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Active les chemins longs qui dépassent **MAX_PATH** de longueur. cet élément est pris en charge dans Windows 10, la version 1607 et les versions ultérieures. Pour plus d’informations, consultez [cet article](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

Spécifie si l’isolation du pilote d’imprimante est activée. La **valeur true** indique qu’elle est activée. Elle n’a pas d’attribut. l’isolation du pilote d’imprimante améliore la fiabilité du service d’impression Windows en permettant aux pilotes d’imprimante de s’exécuter dans des processus distincts du processus dans lequel le spouleur d’impression s’exécute. la prise en charge de l’isolation du pilote d’imprimante a démarré dans Windows 7 et Windows Server 2008 R2. Une application peut déclarer l’isolement du pilote d’imprimante dans son manifeste d’application pour s’isoler du pilote d’imprimante et améliorer sa fiabilité. Autrement dit, l’application ne se bloquera pas si le pilote d’imprimante rencontre une erreur.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

Spécifie si la prise en charge du défilement ultra-haute résolution est activée. La **valeur true** indique qu’elle est activée. Elle n’a pas d’attribut.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Spécifie les informations d’identité d’un [package MSIX fragmenté](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) pour l’application actuelle. cet élément est pris en charge dans Windows 10, la version 2004 et les versions ultérieures.

L’élément **msix** doit se trouver dans l’espace de noms `urn:schemas-microsoft-com:msix.v1` . Il possède les attributs répertoriés dans le tableau suivant.

| Attribut   | Description                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Décrit les informations sur le serveur de publication. cette valeur doit correspondre à l’attribut **Publisher** dans l’élément [identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) de votre manifeste de package fragmenté. |
| **packageName** | Décrit le contenu du package. Cette valeur doit correspondre à l’attribut **Name** de l’élément [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) dans votre manifeste de package fragmenté.    |
| **applicationId**    | Identificateur unique de l’application. Cette valeur doit correspondre à l’attribut **ID** de l’élément [application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) dans le manifeste de votre package épars.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

Substitue l’implémentation du tas par défaut pour les [API de tas Win32](../Memory/heap-functions.md) à utiliser.

* La valeur **SegmentHeap** indique que le segment de mémoire est utilisé. Segment Heap est une implémentation de tas moderne qui réduit généralement l’utilisation globale de la mémoire. cet élément est pris en charge dans Windows 10, version 2004 (build 19041) et versions ultérieures.
* Toutes les autres valeurs sont ignorées.

Cet élément n’a pas d’attributs.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Exemples

Voici un exemple de manifeste d’application pour une application nommée MySampleApp.exe. L’application consomme l’assembly côte à côte SampleAssembly.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
