---
description: Transmet une valeur de clé avec toutes les données associées requises par le module de déchiffrement du contenu pour le système de clé donné.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMFMediaKeySession :: Update, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538263"
---
# <a name="imfmediakeysessionupdate-method"></a>IMFMediaKeySession :: Update, méthode

Transmet une valeur de clé avec toutes les données associées requises par le module de déchiffrement du contenu pour le système de clé donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*libéré* 
</dt> <dd>

Nombre, en octets, de la *clé*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




