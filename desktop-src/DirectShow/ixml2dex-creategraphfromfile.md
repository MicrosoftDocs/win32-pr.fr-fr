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
ms.openlocfilehash: a79b4115dddb0e15adb4284bbefd245aba088d5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007519"
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

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IXml2Dex**](ixml2dex.md)
</dt> </dl>

 

 



