---
description: L’interface ISampleGrabber est exposée par l’exemple de filtre d’accrochage. Il permet à une application de récupérer des exemples de médias individuels lorsqu’ils se déplacent dans le graphique de filtre.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interface ISampleGrabber (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523472"
---
# <a name="isamplegrabber-interface"></a>Interface ISampleGrabber

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’interface **ISampleGrabber** est exposée par l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) . Il permet à une application de récupérer des exemples de médias individuels lorsqu’ils se déplacent dans le graphique de filtre.

## <a name="members"></a>Membres

L’interface **ISampleGrabber** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabber** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISampleGrabber** possède ces méthodes.



| Méthode                                                                | Description                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Récupère une copie de l’exemple que le filtre a reçu le plus récemment.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Non implémenté.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Spécifie une méthode de rappel à appeler sur les exemples entrants.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Spécifie si le filtre d' [**accrochage**](sample-grabber-filter.md) de l’exemple s’arrête une fois que le filtre a reçu un exemple.<br/> |



 

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> </dl>

 

 
