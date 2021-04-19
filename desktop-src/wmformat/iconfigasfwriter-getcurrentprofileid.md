---
title: Méthode IConfigAsfWriter GetCurrentProfileId
description: La méthode GetCurrentProfileId récupère l’ID de profil actuel. (Pour les profils Windows Media format 4,0 uniquement.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Méthode GetCurrentProfileId format Windows Media
- Méthode GetCurrentProfileId format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544154"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>IConfigAsfWriter :: GetCurrentProfileId, méthode

La méthode **GetCurrentProfileId** récupère l’ID de profil actuel. (Pour les profils Windows Media format 4,0 uniquement.)

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwProfileId* \[ à\]
</dt> <dd>

Pointeur vers une variable de type **DWORD** qui reçoit l’ID de profil actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est désormais obsolète, car elle suppose les profils du kit de développement logiciel (SDK) de format Windows Media version 4,0. Utilisez [**IConfigAsfWriter :: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) ou [**IConfigAsfWriter :: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) à la place pour identifier correctement un profil pour la version 7,0 et les versions ultérieures.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 