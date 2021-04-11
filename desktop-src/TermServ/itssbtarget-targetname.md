---
title: Propriété TargetName de ITsSbTarget
description: Spécifie ou récupère le nom de la cible.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propriété TargetName Services Bureau à distance
- TargetName, propriété Services Bureau à distance, ITsSbTarget, interface
- Services Bureau à distance de l’interface ITsSbTarget, propriété TargetName
- TargetName, propriété Services Bureau à distance, ITsSbTargetEx, interface
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030415"
---
# <a name="itssbtargettargetname-property"></a>ITsSbTarget :: TargetName, propriété

Spécifie ou récupère le nom de la cible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **BSTR** qui spécifie le nom de la cible.

## <a name="remarks"></a>Notes

Cette propriété était en lecture seule avant Windows Server 2012.

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

 

 





