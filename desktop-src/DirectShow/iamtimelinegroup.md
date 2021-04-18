---
description: 'L’interface IAMTimelineGroup définit et récupère les propriétés des groupes dans les services d’édition DirectShow (DES). Un groupe contient une ou plusieurs pistes et, éventuellement, une ou plusieurs compositions, qui à leur tour contiennent des éléments sources d’un type uniforme, tels que des vidéos ou des données audio. Les groupes sont les compositions les plus principales dans une chronologie et exposent également l’interface IAMTimelineComp. Une chronologie peut contenir plusieurs groupes. Chaque groupe a les attributs suivants. Type de média associé. Fréquence d’images à laquelle le groupe effectue le rendu, en images par seconde (FPS). Toutes les modifications se produisent à un moment arrondi à la limite d’image la plus proche, comme défini par le paramètre FPS du groupe. Niveau de priorité, pour l’écriture de fichiers avec plusieurs flux du même type de média (par exemple, un fichier AVI en deux vidéos). Pour créer un objet de groupe, appelez IAMTimeline :: CreateEmptyNode avec le \_ groupe de types major de la valeur Timeline \_ \_ . Vous pouvez interroger le pointeur IAMTimelineObj retourné pour l’interface IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interface IAMTimelineGroup (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540096"
---
# <a name="iamtimelinegroup-interface"></a>Interface IAMTimelineGroup

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineGroup` interface définit et récupère des propriétés sur des groupes dans les [services d’édition DirectShow](directshow-editing-services.md) (des).

Un groupe contient une ou plusieurs pistes et, éventuellement, une ou plusieurs compositions, qui à leur tour contiennent des éléments sources d’un type uniforme, tels que des vidéos ou des données audio. Les groupes sont les compositions les plus principales dans une chronologie et exposent également l’interface [**IAMTimelineComp**](iamtimelinecomp.md) . Une chronologie peut contenir plusieurs groupes.

Chaque groupe a les attributs suivants.

-   Type de média associé.
-   Fréquence d’images à laquelle le groupe effectue le rendu, en images par seconde (FPS). Toutes les modifications se produisent à un moment arrondi à la limite d’image la plus proche, comme défini par le paramètre FPS du groupe.
-   Niveau de priorité, pour l’écriture de fichiers avec plusieurs flux du même type de média (par exemple, un fichier AVI en deux vidéos).

Pour créer un objet de groupe, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec le \_ groupe de types major de la valeur Timeline \_ \_ . Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l’interface **IAMTimelineGroup** .

## <a name="members"></a>Membres

L’interface **IAMTimelineGroup** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineGroup** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineGroup** possède ces méthodes.



| Méthode                                                                            | Description                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Non pris en charge.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Récupère le nom défini par l’application du groupe.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Récupère le type de média non compressé pour le groupe.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Récupère le nombre d’images rendues à l’avance pendant la préversion.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Récupère la fréquence d’images de sortie de ce groupe.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Récupère le mode Aperçu pour le groupe.<br/>                                            |
| [**GetPriority,**](iamtimelinegroup-getpriority.md)                               | Récupère la priorité du groupe.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Récupère le format de compression actuel pour la recompression intelligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Récupère la chronologie à laquelle appartient ce groupe.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Non pris en charge.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Détermine si un format de compression intelligente a été défini pour le groupe.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Définit le nom défini par l’application du groupe.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Définit le type de média non compressé pour le groupe.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Spécifie le type de média du groupe pour les clients Automation.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Définit la fréquence d’images de sortie non compressées pour ce groupe.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Définit le mode Aperçu pour le groupe.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Spécifie un format de compression à utiliser pour la recompression intelligente.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | Non pris en charge.<br/>                                                                       |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
