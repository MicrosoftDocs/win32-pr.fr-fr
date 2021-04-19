---
description: L’interface IAMTimelineTransable ajoute DES transitions à un objet dans les services de modification DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interface IAMTimelineTransable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545668"
---
# <a name="iamtimelinetransable-interface"></a>Interface IAMTimelineTransable

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineTransable` interface ajoute des transitions à un objet dans les [services de modification DirectShow](directshow-editing-services.md) (des). Cette interface est exposée par tout objet auquel des transitions peuvent être appliquées, y compris des pistes, des compositions et des groupes. Un objet qui implémente cette interface peut avoir un nombre quelconque de transitions, mais les transitions ne doivent pas se chevaucher dans le temps.

> [!Note]  
> L’audio ne prend pas en charge les transitions. Les objets dans les groupes audio peuvent exposer l' `IAMTimelineTransable` interface, mais l’application ne doit pas lui ajouter de transitions.

 

## <a name="members"></a>Membres

L’interface **IAMTimelineTransable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTransable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineTransable** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure, avec l’heure indiquée comme valeur **REFTIME** .<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Récupère la transition la plus proche de l’heure spécifiée.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Récupère la transition la plus proche de l’heure spécifiée, sous la forme d’une valeur **REFTIME** .<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Ajoute une transition à l’objet.<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Récupère le nombre de transitions sur cet objet.<br/>                                                                     |



 

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



 

 
