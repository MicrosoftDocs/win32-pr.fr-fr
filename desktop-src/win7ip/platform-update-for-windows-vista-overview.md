---
title: à propos de la mise à jour de plateforme pour Windows Vista
description: fournit une vue d’ensemble de la mise à jour de la plateforme pour Windows Vista et de la mise à jour de la plateforme pour Windows Server 2008 et leurs fonctionnalités.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- mise à jour de plateforme pour Windows Server 2008
- mise à jour de plateforme pour Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293182"
---
# <a name="about-platform-update-for-windows-vista"></a>à propos de la mise à jour de plateforme pour Windows Vista

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 sont des mises à jour du système d’exploitation de l’utilisateur final qui prennent en charge l’utilisation des technologies Windows 7 sélectionnées sur les versions précédentes du système d’exploitation Windows. les mises à jour incluent un ensemble de bibliothèques runtime qui permettent aux développeurs d’applications de cibler les versions actuelles, Windows 7 et Windows server 2008 R2, ainsi que les versions précédentes, Windows Vista et Windows server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Résumé de l’API prise en charge par la technologie

chaque technologie prise en charge par la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour les mises à jour Windows Server 2008 comprend un ensemble d’API qui peut être utilisé dans une application qui cible une version antérieure de Windows.

pour plus d’informations sur l’utilisation d’api prises en charge par les mises à jour dans une application qui cible des versions antérieures de Windows, consultez [développement d’applications pour les versions antérieures de Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> certaines api associées à une technologie peuvent ne pas être prises en charge et le comportement, les performances ou les exigences de certaines api prises en charge peuvent varier d’une version à l’autre Windows. Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Technologies prises en charge avec la mise à jour de plateforme pour Windows Vista

Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.

les technologies prises en charge pour Windows vista et Windows XP avec la mise à jour de plateforme pour Windows vista sont présentées dans le tableau suivant.

| Technologie                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API Windows Automation](#windows-automation-api)                                             | Oui           | Oui        |
| [Windows Graphics, Imaging et bibliothèque XPS](#windows-graphics-imaging-and-xps-library)        | Oui           | Non         |
| [Windows Bibliothèque du gestionnaire d’animations et du ruban](#windows-ribbon-and-animation-manager-library) | Oui           | Non         |
| [Windows Plateforme d’appareils mobiles](#windows-portable-devices-platform)                       | Oui           | Non         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Technologies prises en charge avec la mise à jour de plateforme pour Windows Server 2008

Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.

les technologies prises en charge pour Windows server 2008 et Windows server 2003 avec la mise à jour de plateforme pour Windows server 2008 sont présentées dans le tableau suivant.

| Technologie                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API Windows Automation](#windows-automation-api)                                             | Oui                 | Oui                 |
| [Windows Graphics, Imaging et bibliothèque XPS](#windows-graphics-imaging-and-xps-library)        | Oui                 | Non                  |
| [Windows Bibliothèque du gestionnaire d’animations et du ruban](#windows-ribbon-and-animation-manager-library) | Oui                 | Non                  |
| [Windows Plateforme d’appareils mobiles](#windows-portable-devices-platform)                       | Non                  | Non                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descriptions des API prises en charge par la technologie

Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.

-   [API Windows Automation](#windows-automation-api)
-   [Windows Graphics, Imaging et bibliothèque XPS](#windows-graphics-imaging-and-xps-library)
-   [Windows Bibliothèque du gestionnaire d’animations et du ruban](#windows-ribbon-and-animation-manager-library)
-   [Windows Plateforme d’appareils mobiles](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API Windows Automation

Windows L’API Automation 3,0 est un ensemble de dll et d’éléments d’API qui activent les produits de technologie d’assistance pour fournir un meilleur accès informatique aux personnes qui ont des difficultés physiques ou cognitives, des handicaps ou des handicaps. en outre, étant donné que Windows API d’automatisation 3,0 permet aux applications d’accéder aux éléments d’interface utilisateur d’autres applications et de les manipuler, il s’agit d’une technologie idéale pour l’implémentation d’outils de test automatisés.

Microsoft Active Accessibility (MSAA) et UI Automation sont similaires en ce sens que les deux fournissent un moyen d’exposer et de collecter des informations sur les éléments et les contrôles de l’interface utilisateur pour prendre en charge l’accessibilité de l’interface utilisateur et l’automatisation des tests logiciels. ui automation est une implémentation Windows de la spécification ui automation. Il s’agit d’une technologie plus récente qui résout un grand nombre des limitations de MSAA.

pour plus d’informations sur l’api automation de Windows 3,0, consultez Windows de l' [api automation : vue d’ensemble](/windows/desktop/WinAuto/windows-automation-api-overview).

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 prennent en charge l’API d’automatisation des Windows suivante 3,0 :

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [UI Automation](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Éditions éligibles pour les mises à jour

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 activent Windows la prise en charge de l’API Automation 3,0 sur les éditions de Windows présentées dans le tableau suivant.



<table>
<thead>
<tr class="header">
<th>Version de Windows</th>
<th>Éditions éligibles à la mise à jour</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter avec SP2 (x86)<br />
Édition familial de base avec SP2 (x86 et amd64)<br />
Premium d’hébergement avec SP2 (x86 et amd64)<br />
Entreprise avec SP2 (x86 et amd64)<br />
Enterprise avec SP2 (x86 et amd64)<br />
Édition intégrale avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP famille avec SP3 (x86)<br />
Windows XP Professional avec SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Serveur 2008 avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Serveur 2003 avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) est une technologie héritée qui a été introduite pour la première fois avec Windows 95. Il s’agit d’un ensemble d’API qui améliore la façon dont les produits de technologie d’assistance (AT) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows. L’API fournit des interfaces et des méthodes de programmation pour exposer des informations sur les éléments de l’interface utilisateur.

Pour plus d’informations sur Microsoft Active Accessibility, consultez la [Présentation technique](/windows/desktop/WinAuto/technical-overview).

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Éléments de l’API Microsoft Active Accessibility pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="ui-automation"></a>Automatisation de l’interface utilisateur

UI Automation est une technologie plus récente qui implémente la spécification UI Automation et résout un grand nombre des limitations de Microsoft Active Accessibility. Il s’agit d’un ensemble d’API qui fournit un accès par programmation aux éléments de l’interface utilisateur des applications. L’API fournie aide les produits de technologie d’assistance et les outils de test automatisés à accéder, identifier et manipuler les éléments d’interface utilisateur standard et personnalisés d’une application.

pour plus d’informations sur ui automation, consultez [Windows API automation : ui automation](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Éléments d’API UI Automation pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>exécution d’UI Automation sur les Versions antérieures de Windows

en raison des différences dans la façon dont les contrôles communs et les contrôles Windows standard sont implémentés sur différentes versions de Windows, il peut y avoir de légères différences dans les informations que les proxys UI Automation récupèrent pour ces contrôles d’une version à l’autre.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows Graphics, Imaging et bibliothèque XPS

la mise à jour de plateforme pour Windows Vista prend en charge les api Windows 7 suivantes à partir de la bibliothèque Windows graphics, Imaging et XPS :

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Packaging](#packaging)
-   [Composant Windows Imaging](#windows-imaging-component)
-   [Document XPS](#xps-document)
-   [Impression XPS](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Éditions éligibles pour les mises à jour

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 autorisent la prise en charge de Windows graphics, Imaging et XPS sur les éditions de Windows présentées dans le tableau suivant.



<table>
<thead>
<tr class="header">
<th>Version de Windows</th>
<th>Éditions éligibles à la mise à jour</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter avec SP2 (x86)<br />
Édition familial de base avec SP2 (x86 et amd64)<br />
Premium d’hébergement avec SP2 (x86 et amd64)<br />
Entreprise avec SP2 (x86 et amd64)<br />
Enterprise avec SP2 (x86 et amd64)<br />
Édition intégrale avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Serveur 2008 avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

L’API Direct2D est une nouvelle API graphique en 2D en mode immédiat, accélérée par le matériel, qui offre des performances élevées et un rendu de haute qualité pour la géométrie 2D, les bitmaps et le texte. l’API Direct2D est conçue pour interagir correctement avec le code existant qui utilise GDI, GDI+ ou Direct3D.

Pour plus d’informations sur Direct2D, consultez [à propos de Direct2D](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Éléments de l’API Direct2D pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>exécution de Direct2D sur les Versions antérieures de Windows

si le pilote WDDM 1,1 est manquant sur Windows Vista, les performances de l’interopérabilité de Direct2D/GDI sont dégradées.

### <a name="direct3d"></a>Direct3D

la mise à jour de la plateforme pour Windows Vista offre une prise en charge de la surface BGRA pour les chemins de code Direct3D10 et direct3d 10.1. Direct3D10Level9 permet aux fonctionnalités Direct3D10 de fonctionner sur du matériel Direct3D9. Direct3D WARP10 est un rastériseur logiciel performant pour les applications Direct3D10. Direct3D11, la dernière version de Direct3D, offre de nouvelles fonctionnalités, telles que la prise en charge de multithreads améliorée, la polygonalisation, la fonctionnalité de DirectCompute et la liaison de nuanceur dynamique.

Si vous créez des applications qui utilisent Direct3D, le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) https://msdn.microsoft.com/directx/aa937788.aspx) est requis.

Pour plus d’informations sur Direct3D, consultez [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Éléments d’API Direct3D pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

l’api DirectWrite est une nouvelle api de texte qui fournit plusieurs couches de fonctionnalités, notamment la disposition du texte, le traitement des scripts, le rendu des glyphes et le système de polices. DirectWrite utilise les polices OpenType et le rendu ClearType sous-pixel pour améliorer l’expérience de texte fournie par les applications. Le rendu du texte est accéléré par le matériel lorsqu’il est utilisé avec Direct2D.

pour plus d’informations sur la DirectWrite, consultez [présentation des DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>éléments de l’API DirectWrite pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>exécution de DirectWrite sur les Versions Windows précédentes

les problèmes de comportement suivants peuvent affecter l’utilisation de l’API DirectWrite sur les versions Windows précédentes :

-   les Scripts qui ne sont pas nouveaux dans Windows 7 peuvent ne pas s’afficher entièrement correctement dans les versions Windows précédentes.
-   les paramètres régionaux qui ne sont pas disponibles dans les versions précédentes de Windows reviennent au comportement par défaut.
-   le Tuner ClearType n’est pas disponible sur les versions précédentes de Windows.
-   l’interopérabilité GDI a un coût de mémoire plus élevé dans certains scénarios sur les versions précédentes de Windows.

### <a name="packaging"></a>Packaging

la mise à jour de plateforme pour Windows Vista prend en charge un sous-ensemble limité des api de Packaging nécessaires pour effectuer des tâches avec l’API de Document XPS dans des applications non gérées.

Pour plus d’informations sur l’empaquetage des API, consultez [vue d’ensemble](/previous-versions/windows/desktop/opc/packaging-api-overview)de l’API de Packaging.

### <a name="supported-packaging-api-elements"></a>Éléments d’API de Packaging pris en charge

Seules les interfaces de Packaging suivantes sont prises en charge :

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (seules les méthodes suivantes sont prises en charge)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Les API de Packaging prises en charge peuvent être utilisées pour créer des flux de fichiers, ainsi que pour créer et interagir avec l’URI basé sur un package.

### <a name="running-packaging-api-on-previous-windows-versions"></a>exécution de l’API de Packaging sur les Versions antérieures de Windows

Le comportement et les performances des interfaces et méthodes de Packaging prises en charge sont les mêmes sur toutes les plateformes prises en charge.

Si une application tente d’instancier ou d’appeler une méthode ou une interface de Packaging non prise en charge, la tentative échoue. Si l’appel est dirigé vers une méthode [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) non prise en charge, le \_ code d’erreur E NOTIMPL est retourné.

### <a name="windows-imaging-component"></a>Composant Windows Imaging

les nouvelles fonctionnalités du composant de création d’images en Windows (WIC) incluent la sécurité améliorée, la prise en charge de la haute couleur et une meilleure interopérabilité des métadonnées. en outre, le composant de création d’images Windows élargit sa conformité aux normes en fournissant une prise en charge du décodage de l’image progressive, des fonctionnalités PNG étendues, des métadonnées GIF,, des mises à jour de photos HD et des métadonnées qui s’étendent sur les segments APPn.

pour plus d’informations sur le composant de création d’images Windows, consultez la [vue d’ensemble du composant de création d’images Windows](/windows/desktop/wic/-wic-about-windows-imaging-codec).

### <a name="supported-wic-api-elements"></a>Éléments d’API WIC pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="xps-document"></a>Document XPS

Les API de document XPS prennent en charge la création, la modification et l’enregistrement de documents XPS dans des applications non gérées

Pour plus d’informations sur les API de document XPS, consultez le [Guide de programmation de documents XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Éléments de l’API document XPS pris en charge

Seules les interfaces de [signature numérique XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) ne sont pas prises en charge sur les versions de système d’exploitation de niveau supérieur.

### <a name="xps-print"></a>Impression XPS

les api d’impression xps prennent en charge l’impression de documents xps à partir d’applications basées sur Windows.

Pour plus d’informations sur les API d’impression XPS, consultez l' [API XpsPrint](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Éléments de l’API d’impression XPS pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows Bibliothèque du gestionnaire d’animations et du ruban

la mise à jour de la plateforme pour Windows Vista prend en charge les api Windows 7 suivantes à partir du ruban Windows et de la bibliothèque d’Animation :

-   [Windows Infrastructure du ruban](#windows-ribbon-and-animation-manager-library)
-   [Windows Gestionnaire d’animations](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Éditions éligibles pour les mises à jour

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 autorisent la prise en charge de Windows ruban et de la bibliothèque du gestionnaire d’animations sur les éditions de Windows présentées dans le tableau suivant.



<table>
<thead>
<tr class="header">
<th>Version de Windows</th>
<th>Éditions éligibles à la mise à jour</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter avec SP2 (x86)<br />
Édition familial de base avec SP2 (x86 et amd64)<br />
Premium d’hébergement avec SP2 (x86 et amd64)<br />
Entreprise avec SP2 (x86 et amd64)<br />
Enterprise avec SP2 (x86 et amd64)<br />
Édition intégrale avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Serveur 2008 avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows Infrastructure du ruban

l’infrastructure du ruban Windows (ruban) est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.

le framework est une collection d’api Microsoft Win32 qui fournissent une série de nouvelles fonctionnalités d’interface utilisateur pour les développeurs Windows et qui comprend le ruban et un système de menu contextuel.

pour plus d’informations sur l’infrastructure du ruban, consultez [présentation de l’infrastructure du ruban Windows](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Éléments d’API Framework du ruban pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="windows-animation-manager"></a>Windows Gestionnaire d’animations

le gestionnaire d’animations Windows (animation Windows) est une interface de programmation qui prend en charge l’Animation des éléments visuels des applications Windows. Windows L’animation est conçue pour simplifier le développement et la maintenance des séquences d’animation et permettre aux développeurs d’implémenter des animations cohérentes et intuitives. Windows L’animation peut être utilisée avec n’importe quelle plateforme graphique, notamment Direct2D, Direct3D ou GDI+.

Windows L’animation est une API COM à thread unique qui fournit tout ce dont un développeur a besoin pour créer, gérer et générer des animations d’interface utilisateur.

pour plus d’informations sur le gestionnaire d’animations Windows, consultez présentation de l' [animation Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Éléments de l’API du gestionnaire d’animations pris en charge

toutes les api sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Windows Plateforme d’appareils mobiles

la mise à jour de la plateforme pour Windows Vista prend en charge les extensions Windows 7 sur la plateforme des appareils mobiles Windowss (WPD). Cette fonctionnalité permet aux ordinateurs de communiquer avec les périphériques de stockage et les supports associés. WPD offre une méthode flexible et fiable pour les ordinateurs qui communiquent avec les appareils photo numériques, les lecteurs musicaux, les téléphones mobiles et de nombreux autres types d’appareils connectés.

pour plus d’informations sur l’Windows des appareils mobiles, consultez [Windows des appareils mobiles](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Éditions éligibles pour les mises à jour

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 activent la prise en charge des appareils mobiles Windows sur les éditions de Windows présentées dans le tableau suivant.



<table>
<thead>
<tr class="header">
<th>Version de Windows</th>
<th>Éditions éligibles à la mise à jour</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter avec SP2 (x86)<br />
Édition familial de base avec SP2 (x86 et amd64)<br />
Premium d’hébergement avec SP2 (x86 et amd64)<br />
Entreprise avec SP2 (x86 et amd64)<br />
Enterprise avec SP2 (x86 et amd64)<br />
Édition intégrale avec SP2 (x86 et amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Éléments d’API WPD pris en charge

le tableau suivant identifie les fonctionnalités prises en charge pour le Windows 7, Windows vista et Windows vista avec la mise à jour de la plateforme pour les versions Windows vista du système d’exploitation Windows.

| Fonctionnalité WPD                    | Windows 7 | Windows Vista | Windows vista avec la mise à jour de la plateforme pour Windows vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP sur USB                   | Oui       | Oui           | Oui                                                  |
| MTP sur IP                    | Oui       | Oui           | Oui                                                  |
| MTP sur Bluetooth             | Oui       | Non            | Oui                                                  |
| Services d’appareil WPD et MTP    | Oui       | Non            | Oui                                                  |
| Automation WPD                 | Oui       | Non            | Non                                                   |
| Multi-fonctions/transport multiple | Oui       | Non            | Non                                                   |
| Device Stage                   | Oui       | Non            | Non                                                   |
| Plateforme de synchronisation des appareils           | Oui       | Non            | Non                                                   |



 

pour les éditions de Windows 7 et Windows Vista pour lesquelles Microsoft Lecteur Windows Media n’est pas installé par défaut (les éditions N et KN), vous devez installer le [kit de développement logiciel (SDK) Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) pour activer la fonctionnalité WPD). pour plus d’informations, consultez l’article de la [Base de connaissances](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , qui a été publié à l’origine en tant que solution pour Windows Vista.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[mise à jour de plateforme pour Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Vues d'ensemble**
</dt> <dt>

[à propos de la mise à jour de plateforme pour Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[article de la Base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 