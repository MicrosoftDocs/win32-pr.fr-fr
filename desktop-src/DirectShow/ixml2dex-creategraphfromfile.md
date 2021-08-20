---
description: 'Méthode IXml2Dex :: CreateGraphFromFile-non implémentée.'
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: 'IXml2Dex :: CreateGraphFromFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e3ce23fd92a843219490202d42ead4e386deddc8c056b883d2ac45b77a8555d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817066"
---
# <a name="ixml2dexcreategraphfromfile-method"></a>IXml2Dex :: CreateGraphFromFile, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

Non implémenté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppGraph* 
</dt> <dd>

Réservé.

</dd> <dt>

*pTimeline* 
</dt> <dd>

Réservé.

</dd> <dt>

*FileName* 
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IXml2Dex**](ixml2dex.md)
</dt> </dl>

 

 



