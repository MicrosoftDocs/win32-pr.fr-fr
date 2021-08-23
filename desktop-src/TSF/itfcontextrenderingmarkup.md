---
title: Interface ITfContextRenderingMarkup
description: L’interface ITfContextRenderingMarkup est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée à l’aide de IQueryInterface à partir de l’objet ITfContext. Cette interface permet à l’application d’énumérer les informations de rendu.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfContextRenderingMarkup interface Text Services Framework
- ITfContextRenderingMarkup interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80abb7e68e017ec4cd048a7b7df1799578a4d41568b2fcc062ec3845fcf49c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877027"
---
# <a name="itfcontextrenderingmarkup-interface"></a>Interface ITfContextRenderingMarkup

L’interface **ITfContextRenderingMarkup** est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée à l’aide de IQueryInterface à partir de l’objet [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) . Cette interface permet à l’application d’énumérer les informations de rendu.



| Méthodes ITfContextRenderingMarkup                                                | Description                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Récupère un énumérateur des balises de rendu pour la plage donnée. |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Cette fonction n’est pas implémentée. Elle retourne toujours E \_ NOTIMPL.       |



 

## <a name="members"></a>Membres

L’interface **ITfContextRenderingMarkup** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette interface n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

 