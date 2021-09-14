---
description: l’interface IAMSetErrorLog définit ou récupère un journal des erreurs dans DirectShow Services d’édition (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interface IAMSetErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234096"
---
# <a name="iamseterrorlog-interface"></a>Interface IAMSetErrorLog

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMSetErrorLog` interface définit ou récupère un journal des erreurs dans [DirectShow Services d’édition](directshow-editing-services.md) (DES). L’objet Timeline implémente cette interface. Les applications peuvent utiliser cette interface pour consigner les erreurs de rendu au moment de l’exécution. Implémentez l’interface [**IAMErrorLog**](iamerrorlog.md) dans votre application, puis appelez la méthode [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie.

Pour plus d’informations sur l’utilisation de cette interface, consultez [journalisation des erreurs](logging-errors.md).

## <a name="members"></a>Membres

L’interface **IAMSetErrorLog** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMSetErrorLog** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMSetErrorLog** possède ces méthodes.



| Méthode                                               | Description                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**recevoir le \_ Journal des erreurs**](iamseterrorlog-get-errorlog.md) | Récupère le journal des erreurs actuel de cet objet.<br/> |
| [**Placer le \_ Journal des erreurs**](iamseterrorlog-put-errorlog.md) | Spécifie un journal des erreurs pour l’objet.<br/>           |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
