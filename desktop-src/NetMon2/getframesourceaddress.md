---
description: Récupère l’adresse source d’un frame.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: GetFrameSourceAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4878e08b8d8fb475c0da23d2ed765819fa14a10cd93140c791ed8603b1677584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366316"
---
# <a name="getframesourceaddress-function"></a>GetFrameSourceAddress fonction)

La fonction **GetFrameSourceAddress** récupère l’adresse source d’un frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle vers le frame auquel un pointeur doit être obtenu.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Mémoire tampon de retour qui stocke l’adresse de la source du frame.

</dd> <dt>

*Typedadresse* 
</dt> <dd>

Type d’adresse recherchée, par exemple, \_ type d’adresse \_ Ethernet ou adresse IP du type d’adresse \_ \_ .

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Indicateurs utilisés pour modifier les données d’adresse source retournées.



| Valeur                                                                                                                                                                                                           | Signification                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**\_normaliser les indicateurs ADDRESSTYPE \_**</dt> </dl>        | Annule les BITs de routage et de groupe.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**\_bit des indicateurs ADDRESSTYPE \_ \_ inversé**</dt> </dl> | Rétablit la valeur normale des adresses réseau Token Ring.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur *lpAddress* est valide et la valeur de retour est BHERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                                | Description                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_protocole BHERR \_ \_ introuvable**</dt> </dl> | Le protocole spécifié par le paramètre *AddressType* n’est pas valide pour le frame.<br/> |
| <dl> <dt>**BHERR \_ non valide \_ HFRAME**</dt> </dl>      | La valeur du paramètre *hFrame* n’est pas valide.<br/>                                        |



 

## <a name="remarks"></a>Remarques

Le type d’adresse **\_ \_ \_ le plus élevé** est autorisé. Lorsque ce type d’adresse est utilisé, la fonction recherche l’adresse IP IPX, XNS, IP ou VINEs avant de renvoyer l’adresse ETHERNET, TOKENRING ou FDDI. Cette approche est utile pour les protocoles et les environnements dans lesquels deux cartes réseau peuvent être multiplexées sous une seule adresse de serveur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




