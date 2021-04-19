---
description: L’interface IAMErrorLog fournit une méthode de rappel pour la journalisation des erreurs dans les services de modification DirectShow (DES). DES n’implémente pas cette interface.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interface IAMErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537452"
---
# <a name="iamerrorlog-interface"></a>Interface IAMErrorLog

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMErrorLog` interface fournit une méthode de rappel pour la journalisation des erreurs dans les [services de modification DirectShow](directshow-editing-services.md) (des).

DES n’implémente pas cette interface. Pour effectuer la journalisation des erreurs, implémentez cette interface dans votre application et appelez [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie. Si une erreur se produit lors du rendu du projet, les appellent la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) implémentée par votre application.

DES enregistre les erreurs uniquement lorsque vous affichez un projet à l’aide de l’interface [**IRenderEngine**](irenderengine.md) . Par exemple, si vous enregistrez un projet sous la forme d’un graphique de filtre DirectShow (format. GRF) et que vous lisez le fichier de graphique, il n’y a pas de journalisation des erreurs. Pour plus d’informations sur l’utilisation de cette interface, consultez [journalisation des erreurs](logging-errors.md).

## <a name="members"></a>Membres

L’interface **IAMErrorLog** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMErrorLog** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMErrorLog** possède ces méthodes.



| Méthode                                   | Description               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Enregistre une erreur.<br/> |



 

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



 

 
