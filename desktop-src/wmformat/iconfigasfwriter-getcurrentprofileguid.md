---
title: Méthode IConfigAsfWriter GetCurrentProfileGuid
description: la méthode GetCurrentProfileGuid récupère le GUID actuel du profil de système multimédia Windows.
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
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433638"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter :: GetCurrentProfileGuid, méthode

la méthode **GetCurrentProfileGuid** récupère le GUID actuel du profil de système multimédia Windows.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
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

## <a name="remarks"></a>Remarques

cette méthode n’est pas utilisée avec les profils personnalisés (y compris tous les profils qui incluent des flux qui utilisent les codecs Windows Media Audio et vidéo), car tous ces profils sont créés par des applications et n’ont pas d’identificateur GUID. Si aucun profil système n’est chargé, *pProfileGuid* prend la valeur **null**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 