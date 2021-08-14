---
title: Méthode IConfigAsfWriter GetCurrentProfileId
description: La méthode GetCurrentProfileId récupère l’ID de profil actuel. (pour les profils Windows Media Format 4,0 uniquement.).
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
ms.openlocfilehash: e065e15b0c73b4b1037003dee936af5f74208e4433c6925594e18ab92319028c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655474"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>IConfigAsfWriter :: GetCurrentProfileId, méthode

La méthode **GetCurrentProfileId** récupère l’ID de profil actuel. (pour les profils Windows Media Format 4,0 uniquement.)

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
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

## <a name="remarks"></a>Remarques

cette méthode est désormais obsolète, car elle suppose la version 4,0 Windows les profils du kit de développement logiciel (SDK) de Format multimédia. Utilisez [**IConfigAsfWriter :: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) ou [**IConfigAsfWriter :: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) à la place pour identifier correctement un profil pour la version 7,0 et les versions ultérieures.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 