---
description: Méthode de constructeur.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Constructeur CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515735"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Constructeur CPosPassThru. CPosPassThru

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de l’objet, à des fins de débogage. Allouez ce paramètre dans la mémoire statique.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Ignoré.

</dd> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du filtre.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



