---
description: Crée un objet de session de clé multimédia à l’aide des données d’initialisation et des données personnalisées spécifiées. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMFMediaKeys :: CreateSession, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2dd9bcc7a1151b042d275917e8bd8106eb079de3315137ca41fa7faecaf5c957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942039"
---
# <a name="imfmediakeyscreatesession-method"></a>IMFMediaKeys :: CreateSession, méthode

Crée un objet de session de clé multimédia à l’aide des données d’initialisation et des données personnalisées spécifiées. .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mimeType* 
</dt> <dd>

Type MIME du conteneur multimédia utilisé pour le contenu.

</dd> <dt>

*initData* 
</dt> <dd>

Données d’initialisation du système de clés.

</dd> <dt>

*libéré* 
</dt> <dd>

Nombre, en octets, *initData*.

</dd> <dt>

*customData* 
</dt> <dd>

Données personnalisées envoyées au système de clés.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

Nombre, en octets, de *cbCustomData*.

</dd> <dt>

*indiquer* 
</dt> <dd>

indiquer

</dd> <dt>

*ppSession* 
</dt> <dd>

Session de la clé du média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




