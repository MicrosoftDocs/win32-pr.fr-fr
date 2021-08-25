---
description: Contient la méthode utilisée pour obtenir un point de terminaison utilisé pour se connecter à un service.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interface IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896839"
---
# <a name="iupdateendpointprovider-interface"></a>Interface IUpdateEndpointProvider

Contient la méthode utilisée pour obtenir un point de terminaison utilisé pour se connecter à un service. Cette interface est implémentée lors de l’écriture d’un fournisseur de points de terminaison.

## <a name="members"></a>Membres

L’interface **IUpdateEndpointProvider** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointProvider** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUpdateEndpointProvider** possède ces méthodes.



| Méthode                                                                       | Description                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Demande un point de terminaison utilisé pour se connecter à un service.<br/> |



 

## <a name="remarks"></a>Remarques

WUA appelle la méthode [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) pour démarrer le processus de négociation. Lorsque l’appel est effectué, WUA passe les types de jetons inscrits et l’implémentation de cette interface retourne les types de jetons qu’il préfère utiliser.

 

 
