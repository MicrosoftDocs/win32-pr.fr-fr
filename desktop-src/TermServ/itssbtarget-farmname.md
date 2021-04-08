---
title: ITsSbTarget propriété FarmName
description: Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678413"
---
# <a name="itssbtargetfarmname-property"></a>ITsSbTarget :: FarmName, propriété

Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **BSTR** qui contient le nom de la batterie de serveurs.

## <a name="requirements"></a>Configuration requise



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Client minimal pris en charge<br/></td>
<td>Aucun pris en charge<br/></td>
</tr>
<tr class="even">
<td>Serveur minimal pris en charge<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>MIDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget est défini comme suit :
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-DB0B-4752-B456-5fd5840901c0 sur Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





