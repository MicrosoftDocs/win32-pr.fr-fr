---
title: Méthode IConfigAsfWriter GetCurrentProfileGuid
description: La méthode GetCurrentProfileGuid récupère le GUID du profil de système Windows Media actuel.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Méthode GetCurrentProfileGuid format Windows Media
- Méthode GetCurrentProfileGuid format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316127"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter :: GetCurrentProfileGuid, méthode

La méthode **GetCurrentProfileGuid** récupère le GUID du profil de système Windows Media actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProfileGuid* \[ à\]
</dt> <dd>

Pointeur vers une variable de type **GUID** qui identifie le profil système actuel utilisé par le filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode n’est pas utilisée avec les profils personnalisés (y compris tous les profils qui incluent des flux qui utilisent les codecs Windows Media Audio et vidéo), car tous ces profils sont créés par des applications et n’ont pas d’identificateur GUID. Si aucun profil système n’est chargé, *pProfileGuid* prend la valeur **null**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 