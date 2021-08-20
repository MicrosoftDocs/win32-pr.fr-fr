---
description: 'L’interface ISampleGrabberCB fournit des méthodes de rappel pour la méthode ISampleGrabber :: SetCallback. Si votre application appelle cette méthode, elle doit implémenter cette interface. Pour plus d’informations, consultez ISampleGrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interface ISampleGrabberCB (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 822eef97ebd2ff169631f0e4d83cdfe3417388389e112851f5e77dcd7216acfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817501"
---
# <a name="isamplegrabbercb-interface"></a>Interface ISampleGrabberCB

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `ISampleGrabberCB` interface fournit des méthodes de rappel pour la méthode [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md) . Si votre application appelle cette méthode, elle doit implémenter cette interface. Pour plus d’informations, consultez [**ISampleGrabber**](isamplegrabber.md).

## <a name="members"></a>Membres

L’interface **ISampleGrabberCB** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabberCB** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISampleGrabberCB** possède ces méthodes.



| Méthode                                        | Description                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Méthode de rappel qui reçoit un pointeur vers l’exemple de média.<br/>  |



 

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



 

 
