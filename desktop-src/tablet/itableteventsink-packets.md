---
description: Se produit lorsque le stylet se déplace sur le digitaliseur.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink ::P méthode ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952425"
---
# <a name="itableteventsinkpackets-method"></a>ITabletEventSink ::P méthode ackets

Se produit lorsque le stylet se déplace sur le digitaliseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur de la tablette.

</dd> <dt>

*cPkts* \[ dans\]
</dt> <dd>

Nombre de paquets.

</dd> <dt>

*cbPkts* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon des paquets

</dd> <dt>

*pbPkts* \[ dans\]
</dt> <dd>

Mémoire tampon de paquets.

</dd> <dt>

*pnSerialNumbers* \[ dans\]
</dt> <dd>

Tableau des numéros de série.

</dd> <dt>

*confirmation* 
</dt> <dd>

Identificateur du stylet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




