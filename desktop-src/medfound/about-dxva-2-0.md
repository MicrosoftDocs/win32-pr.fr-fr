---
description: Vue d’ensemble d’DXVA 2 et de sa relation avec DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: À propos de DXVA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236405"
---
# <a name="about-dxva-20"></a>À propos de DXVA 2,0

DirectX Video Acceleration (DXVA) est une API et une interface DDI correspondante pour l’utilisation de l’accélération matérielle pour accélérer le traitement vidéo. Les codecs logiciels et les processeurs vidéo logiciels peuvent utiliser la fonctionnalité DXVA pour décharger certaines opérations gourmandes en ressources du processeur vers le GPU. Par exemple, un décodeur logiciel peut décharger la transformation de cosinus discrète inverse (iDCT) sur le GPU.

Dans DXVA, certaines opérations de décodage sont implémentées par le pilote matériel Graphics. Cet ensemble de fonctionnalités est appelé l' *accélérateur*. D’autres opérations de décodage sont implémentées par le logiciel d’application en mode utilisateur, appelé *décodeur hôte* ou *décodeur logiciel*. (Les termes *décodeur hôte* et *décodeur logiciel* sont équivalents.) Le traitement effectué par l’accélérateur est appelé *traitement hors hôte*. En général, l’accélérateur utilise le GPU pour accélérer certaines opérations. Chaque fois que l’accélérateur effectue une opération de décodage, le décodeur hôte doit communiquer avec les mémoires tampons d’accélérateur contenant les informations nécessaires à l’exécution de l’opération

l’API DXVA 2 requiert Windows Vista ou version ultérieure. l’API DXVA 1 est toujours prise en charge dans Windows Vista pour la compatibilité descendante. Une couche d’émulation est fournie, qui convertit entre les deux versions de l’API et la version opposée de la DDI :

-   si le pilote graphique est conforme au modèle WDDM (Windows Display driver Model), les appels d’API dxva 1 sont convertis en appels DDI dxva 2.
-   si les pilotes graphics utilisent l’ancien modèle de pilote d’affichage (XPDM) Windows XP, les appels de l’API dxva 2 sont convertis en appels DDI dxva 1.

Le tableau suivant présente la configuration requise du système d’exploitation et les convertisseurs vidéo pris en charge pour chaque version de l’API DXVA.



| Version d'API | Spécifications          | Prise en charge des convertisseurs vidéo                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 ou version ultérieure | superposition Mixer, vmr-7, vmr-9 (DirectShow uniquement) |
| DXVA 2      | Windows Vista         | EVR (DirectShow et Media Foundation)         |



 

Dans DXVA 1, le décodeur logiciel doit accéder à l’API via le convertisseur vidéo. Il n’existe aucun moyen d’utiliser l’API DXVA 1 sans appeler le convertisseur vidéo. Cette limitation a été supprimée avec DXVA 2. À l’aide de DXVA 2, le décodeur hôte (ou toute application) peut accéder directement à l’API, via l’interface [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .

La documentation DXVA 1 décrit les structures de décodage utilisées pour les normes vidéo suivantes :

-   ITU-T Rec. H. 261
-   ITU-T Rec. H. 263
-   Vidéo MPEG-1
-   Vidéo sur le profil principal MPEG-2

Les spécifications suivantes définissent des extensions DXVA pour d’autres normes vidéo :

-   [Spécification DXVA pour le décodage H. 264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Spécification DXVA pour le codage vidéo MVC H. 264/MPEG-4 AVC (MVC), y compris le profil stéréo High](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Spécification DXVA pour le décodage vidéo MPEG-1 VLD et MPEG-1/MPEG-2 VLD](https://www.microsoft.com/download/details.aspx?id=9374).
-   [Spécification DXVA pour Off-Host mode VLD pour le décodage vidéo MPEG-4 part 2](https://www.microsoft.com/download/details.aspx?id=21100)
-   [spécification DXVA pour le décodage Windows Media Video® v8, v9 et vA (y compris SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Spécification DirectX Video Acceleration (DXVA) pour le décodage en mode VLD (SVC Off-Host) H. 264/MPEG-4](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Spécification de l’accélération vidéo DirectX pour le codage vidéo VP8 et VP9](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 et DXVA 2 utilisent les mêmes structures de données pour le décodage. Toutefois, la procédure de configuration de la session de décodage a changé. DXVA 1 utilise un mécanisme de « sondage et de verrouillage », dans lequel le décodeur de l’hôte peut tester différentes configurations avant de définir la configuration souhaitée sur l’accélérateur. Dans DXVA 2, l’accélérateur retourne une liste des configurations prises en charge et le décodeur hôte en sélectionne un dans la liste. Les détails sont fournis dans les sections suivantes :

-   [Prise en charge de DXVA 2,0 dans DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Spécification 1,0 DXVA](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
