---
title: Méthode IConfigAsfWriter GetCurrentProfile
description: La méthode GetCurrentProfile récupère le profil défini par l’application.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Méthode GetCurrentProfile format Windows Media
- Méthode GetCurrentProfile format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198380"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>IConfigAsfWriter :: GetCurrentProfile, méthode

La méthode **GetCurrentProfile** récupère le profil défini par l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppProfile* \[ à\]
</dt> <dd>

Adresse d’un pointeur qui reçoit l’interface [**IWMProfile**](iwmprofile.md) du profil défini par l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si la méthode est réussie, le pointeur **IWMProfile** retourné a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 