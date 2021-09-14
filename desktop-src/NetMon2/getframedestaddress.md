---
description: Récupère l’adresse de destination d’un frame.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: GetFrameDestAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119258"
---
# <a name="getframedestaddress-function"></a>GetFrameDestAddress fonction)

La fonction **GetFrameDestAddress** récupère l’adresse de destination d’un frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameDestAddress(
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

Handle du frame vers lequel obtenir un pointeur.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Mémoire tampon de retour qui stocke l’adresse de destination du frame.

</dd> <dt>

*Typedadresse* 
</dt> <dd>

Type d’adresse (par exemple, type d’adresse \_ \_ Ethernet ou adresse IP de type d’adresse) \_ \_ .

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Indicateurs utilisés pour modifier les données d’adresse de destination retournées.



| Valeur                                                                                                                                                                                                           | Signification                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**\_normaliser les indicateurs ADDRESSTYPE \_**</dt> </dl>        | Annule les BITs de routage et de groupe.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**\_bit des indicateurs ADDRESSTYPE \_ \_ inversé**</dt> </dl> | Rétablit la valeur normale des adresses réseau Token Ring.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur *lpAddress* est valide et la valeur de retour est BHERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                                | Description                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_protocole BHERR \_ \_ introuvable**</dt> </dl> | Le protocole spécifié dans le paramètre *AddressType* n’est pas valide pour le frame.<br/> |
| <dl> <dt>**BHERR \_ non valide \_ HFRAME**</dt> </dl>      | La valeur *hFrame* n’est pas valide.<br/>                                                  |



 

## <a name="remarks"></a>Notes

Le type d’adresse Rechercher le type d’adresse le **\_ \_ \_ plus élevé** est autorisé. Lorsque ce type d’adresse est utilisé, la fonction recherche l’adresse IP IPX, XNS, IP ou VINEs avant de renvoyer l’adresse ETHERNET, TOKENRING ou FDDI. Cette approche est utile pour les protocoles et dans les environnements où deux cartes réseau peuvent être multiplexées sous une seule adresse de serveur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




