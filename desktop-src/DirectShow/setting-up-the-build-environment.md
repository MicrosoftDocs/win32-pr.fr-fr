---
description: Création d’applications DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Création d’applications DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519174"
---
# <a name="building-directshow-applications"></a>Création d’applications DirectShow

Cette rubrique décrit les en-têtes et les bibliothèques nécessaires pour créer des applications DirectShow.

Les derniers en-têtes et bibliothèques DirectShow sont disponibles dans le [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx).

## <a name="header-files"></a>Fichiers d’en-tête

Toutes les applications DirectShow utilisent le fichier d’en-tête indiqué dans le tableau suivant.



| Fichier d'en-tête | Requis pour                 |
|-------------|------------------------------|
| DShow. h     | Toutes les applications DirectShow. |



 

Certaines interfaces DirectShow requièrent des fichiers d’en-tête supplémentaires. Ces exigences sont indiquées dans la référence de l’interface.

## <a name="library-files"></a>Fichiers de bibliothèque

DirectShow utilise les fichiers de bibliothèque statique indiqués dans le tableau suivant.



| Fichier bibliothèque | Description                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids. lib | Exporte les identificateurs de classe (CLSID) et les identificateurs d’interface (IID).                                                           |
| Quartz. lib   | Exporte la fonction [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) . Si vous n’appelez pas cette fonction, cette bibliothèque n’est pas requise. |



 

Utilisez les mêmes fichiers. lib pour les versions Debug et Release.

## <a name="filter-base-classes"></a>Filtrer les classes de base

L’SDK Windows fournit un ensemble de classes C++ recommandées si vous écrivez un filtre DirectShow personnalisé. Ces classes sont fournies en tant qu’exemple de code, que vous pouvez compiler dans une bibliothèque statique. Pour plus d’informations, consultez [classes de base DirectShow](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>Dll redistribuables

Les applications DirectShow écrites pour Windows XP avec Service Pack 2 (SP2) et versions ultérieures n’ont pas besoin de redistribuer les dll DirectShow.

Pour Windows XP avec Service Pack 1 (SP1) et versions antérieures, les dll DirectShow redistribuables sont disponibles dans le kit de développement logiciel (SDK) Microsoft DirectX. La version la plus récente de ces dll est la version 9.0 c. Aucun développement supplémentaire de ces dll redistribuables n’est prévu. Windows XP avec Service Pack 2 (SP2) contient les dll c version 9.0.

Les packages redstributable contiennent les dll suivantes :

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de filtres DirectShow](building-directshow-filters.md)
</dt> </dl>

 

 
