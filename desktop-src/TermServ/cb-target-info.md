---
title: Structure CB_TARGET_INFO (Cbclient. h)
description: Contient des informations sur l’ordinateur cible et les adresses IP où les connexions entrantes doivent être redirigées.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO structure Services Bureau à distance
- Pointeur de structure PCB_TARGET_INFO Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e7c00e1997ee36b42b21b833942597d9b43f393b2bcdfcee1aa0ee18e3a4548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001607"
---
# <a name="cb_target_info-structure"></a>Structure des informations de la \_ cible CB \_

Contient des informations sur l’ordinateur cible et les adresses IP où les connexions entrantes doivent être redirigées. Cette structure est utilisée avec la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ServerName**
</dt> <dd>

Représente le nom de domaine complet du serveur cible. Pour un scénario de virtualisation des Bureau à distance (RDV), ce membre a la **valeur null**. Dans le cas d’un scénario d’hôte de session Bureau à distance, ce membre contient le nom du serveur sur lequel la connexion entrante est redirigée.

</dd> <dt>

**AddressCount**
</dt> <dd>

Nombre d’entrées valides dans le tableau d' **adresses** .

</dd> <dt>

**Adresses**
</dt> <dd>

Tableau de chaînes qui contient les adresses IP où les connexions entrantes sont redirigées. Le nombre d’éléments valides dans ce tableau est spécifié dans le membre **AddressCount** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





