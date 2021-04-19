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
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514639"
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



 

## <a name="remarks"></a>Notes

WUA appelle la méthode [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) pour démarrer le processus de négociation. Lorsque l’appel est effectué, WUA passe les types de jetons inscrits et l’implémentation de cette interface retourne les types de jetons qu’il préfère utiliser.

 

 
