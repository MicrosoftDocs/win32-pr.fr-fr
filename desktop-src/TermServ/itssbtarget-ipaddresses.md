---
title: Propriété ITsSbTarget adressesIP
description: Récupère ou spécifie les adresses IP externes de la cible.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TargetExternalIpAddresses
- Services Bureau à distance de la propriété TargetExternalIpAddresses, interface ITsSbTarget
- Services Bureau à distance de la propriété TargetExternalIpAddresses, interface ITsSbTarget
- Propriété adressesIP Services Bureau à distance
- Propriété adressesIP Services Bureau à distance, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété adressesIP
- Propriété adressesIP Services Bureau à distance, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété adressesIP
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ff06e60f125590154a17cb7467deae3611a617b684e9068439c9e15609d8fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351250"
---
# <a name="itssbtargetipaddresses-property"></a>ITsSbTarget :: adressesIP, propriété

Récupère ou spécifie les adresses IP externes de la cible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers un tableau de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) qui reçoivent les adresses IP externes de la cible.

Pointeur vers une variable **DWORD** qui contient le nombre d’adresses IP externes dans le paramètre *sockaddr* . Si le nombre d’adresses est inconnu, transmettez *sockaddr* comme **null**. La méthode retourne le nombre de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) nécessaires à l’allocation dans le tableau pointé par le paramètre *sockaddr* .

## <a name="remarks"></a>Remarques

cette propriété était anciennement appelée **TargetExternalIpAddresses** dans Windows Server 2008 R2.

Si le nombre d’adresses IP externes est inconnu, vous pouvez appeler cette méthode avec *sockaddr* défini sur la **valeur null**. La méthode retourne ensuite, dans le paramètre *numAddresses* , le nombre de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) nécessaires pour recevoir toutes les adresses IP externes. Allouez le tableau pour *sockaddr* en fonction de ce nombre, puis appelez à nouveau la méthode, en affectant à *sockaddr* le tableau nouvellement alloué et *numAddresses* au nombre retourné par le premier appel.

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
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 sur Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





