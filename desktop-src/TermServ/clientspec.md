---
title: Énumération ClientSpec
description: Utilisé avec la propriété ClientProtocolSpec pour spécifier le Protocole Bureau à distance utilisé entre le client et le serveur.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857134"
---
# <a name="clientspec-enumeration"></a>Énumération ClientSpec

Utilisé avec la propriété [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) pour spécifier le Protocole Bureau à distance utilisé entre le client et le serveur.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**
</dt> <dd>

le protocole est complet Windows 8 protocole Bureau à distance.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**
</dt> <dd>

le protocole est limité à l’utilisation du codec de RemoteFX Windows 7 avec SP1 et d’un cache plus petit. Tous les autres codecs sont désactivés. Ce protocole présente l’encombrement mémoire le plus faible.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**
</dt> <dd>

Le protocole est identique à **FullMode**, à ceci près qu’il utilise un cache plus petit.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





