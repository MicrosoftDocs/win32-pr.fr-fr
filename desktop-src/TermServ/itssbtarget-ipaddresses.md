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
ms.openlocfilehash: d9021a14977f532c176faa01362aa3b1910d2c9c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482105"
---
# <a name="itssbtargetipaddresses-property"></a>ITsSbTarget :: adressesIP, propriété

Récupère ou spécifie les adresses IP externes de la cible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


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




| | | Client minimal pris en charge<br /> | Aucun pris en charge<br /> | | Serveur minimal pris en charge<br /> | Windows Server 2012<br /> | | MIDL<br /> | <dl><dt>Sbtsv. idl</dt></dl> | | VAUT<br /> | IID_ITsSbTarget est défini comme suit :<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 sur Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





