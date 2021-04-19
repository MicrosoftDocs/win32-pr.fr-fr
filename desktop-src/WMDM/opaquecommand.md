---
title: OPAQUECOMMAND, structure
description: La structure OPAQUECOMMAND contient des données pour les commandes qui sont transmises par le biais de Windows Media Gestionnaire de périphériques à un appareil, mais qui ne sont pas destinées à être traitées par Windows Media Gestionnaire de périphériques.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Structure OPAQUECOMMAND Windows Media Gestionnaire de périphériques
- structure du Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545484"
---
# <a name="opaquecommand-structure"></a>OPAQUECOMMAND, structure

La structure **OPAQUECOMMAND** contient des données pour les commandes qui sont transmises par le biais de windows media gestionnaire de périphériques à un appareil, mais qui ne sont pas destinées à être traitées par windows media gestionnaire de périphériques.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID** représentant la commande demandée.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Longueur des données vers laquelle *pData* pointe, en octets.

</dd> <dt>

**pData**
</dt> <dd>

Données requises pour exécuter la commande et/ou les données retournées par la commande.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Ce code d’authentification de message (MAC) doit inclure le membre **guidCommand** , les données auxquelles *pdwDataLen* pointe, ainsi que les données auxquelles *pData* pointe, le cas échéant. Si *pData* a la **valeur null**, il ne doit pas être inclus dans le Mac. La \_ longueur WMDM Mac \_ est définie sur 20.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





