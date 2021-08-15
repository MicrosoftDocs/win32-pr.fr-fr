---
description: l’interface IAMTimelineSrc fournit des méthodes pour manipuler et définir des propriétés sur les objets sources dans les Services d’édition de DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interface IAMTimelineSrc (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5d2ad5684df6298bde458e87ff322b21622139930fa9aaf994fda0e7ba7e987e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399196"
---
# <a name="iamtimelinesrc-interface"></a>Interface IAMTimelineSrc

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineSrc` interface fournit des méthodes pour la manipulation et la définition des propriétés sur les objets sources dans les [Services d’édition de DirectShow](directshow-editing-services.md) (DES). Un objet source représente un flux d’une source de média.

Vous pouvez utiliser une partie des données d’un fichier source en définissant les heures de démarrage et d’arrêt du support. Ces valeurs spécifient le début et la fin de l’objet source, par rapport à la source du média d’origine. Les temps de support peuvent différer de l’heure de début et de fin de l’objet sur la chronologie, ce qui permet une lecture rapide ou lente. (Avec des sources audio, le décalage de hauteur se produit.)

Pour créer un objet source, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la valeur Timeline \_ principale \_ type \_ source. Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l’interface **IAMTimelineSrc** . Pour plus d’informations, consultez [construction d’une chronologie](constructing-a-timeline.md) et [utilisation de sources](working-with-sources.md).

## <a name="members"></a>Membres

L’interface **IAMTimelineSrc** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSrc** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineSrc** possède ces méthodes.



| Méthode                                                    | Description                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Arrondit les valeurs d’heure spécifiées, sous la forme de valeurs **REFTIME** , à la limite d’image la plus proche.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Récupère la fréquence d’images par défaut de l’objet source.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Récupère la longueur du média de cet objet source.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Récupère la longueur du média de cet objet source, sous la forme d’une valeur **REFTIME** .<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | Récupère le nom du fichier source représenté par cet objet source.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Récupère les heures de démarrage et d’arrêt du média.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Récupère les heures de début et de fin du média, en tant que valeurs **REFTIME** .<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Récupère le numéro de flux actuel de l’objet source.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Récupère le mode stretch d’une source vidéo.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indique si le clip sera lu à la vitesse de lecture normale.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Définit l’heure d’arrêt, par rapport à la chronologie.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Définit l’heure d’arrêt en tant que valeur **REFTIME** .<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Définit la fréquence d’images par défaut de l’objet source.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Spécifie la durée du fichier source.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Spécifie la durée du fichier source, en tant que valeur **REFTIME** .<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | Spécifie le nom du fichier source représenté par cet objet source.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Définit l’heure de début et l’arrêt du support.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Définit l’heure de début et l’arrêt du support, en tant que valeurs **REFTIME** .<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Spécifie le flux à lire à partir du fichier source associé à cet objet source.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Définit le mode d’étirement d’une source vidéo.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Joint cet objet source à un autre objet source.<br/>                                            |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
