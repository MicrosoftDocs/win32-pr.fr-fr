---
title: Structure WINBIO_EVENT ( \_ types WINBIO. h)
description: Contient les informations d’État envoyées à la routine de rappel lorsqu’une notification d’événement est déclenchée.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EVENT
- API du pointeur de structure PWINBIO_EVENT Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3baab16ee7c3f825f317d7aa2c585cb4d8ae7d6d030b6f59a1555b95343015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910542"
---
# <a name="winbio_event-structure"></a>\_Structure d’événement WINBIO

La structure d' **\_ événement WINBIO** contient les informations d’État envoyées à la routine de rappel lorsqu’une notification d’événement est déclenchée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Valeur qui spécifie le type d’avis d’événement du fournisseur de services déclenché. Le seul fournisseur actuellement pris en charge est le capteur d’empreintes digitales. Ce capteur prend en charge les indicateurs suivants.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ ÉVÉNEMENT \_ FP non \_ réclamé** (le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus. le Windows Biometric Framework appelle la fonction de rappel pour indiquer qu’un glissement finger s’est produit, mais n’essaie pas d’identifier l’empreinte digitale.
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ \_ \_ \_ Identification non revendiquée du FP d’événement** (le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus. le Windows Biometric Framework tente d’identifier l’empreinte digitale et transmet le résultat de ce processus à votre fonction de rappel.)
</dt> </dl> </dd> <dt>

**Paramètres**
</dt> <dd> <dl> <dt>

**Revendication**
</dt> <dd>

Structure retournée pour l’exemple de capture biométrique.

<dl> <dt>

**UnitId**
</dt> <dd>

Unité biométrique qui a généré l’exemple.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valeur **ULong** qui contient des informations supplémentaires sur l’échec de la capture d’un échantillon biométrique. Si une capture a réussi, ce paramètre a la valeur zéro. Les valeurs suivantes sont définies pour la capture d’empreinte digitale :

-   WINBIO \_ FP \_ trop \_ élevé
-   WINBIO \_ FP \_ trop \_ faible
-   WINBIO \_ FP \_ trop à \_ gauche
-   WINBIO \_ FP \_ trop à \_ droite
-   WINBIO \_ FP \_ trop \_ Fast
-   WINBIO \_ FP \_ trop \_ lent
-   \_ \_ qualité médiocre de WINBIO FP \_
-   WINBIO \_ FP \_ trop \_ incliné
-   WINBIO \_ FP \_ trop \_ petit
-   échec de la \_ fusion WINBIO FP \_ \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Structure retournée pour la capture et l’identification biométriques. L’identification détermine si un exemple peut être associé à un modèle biométrique existant.

<dl> <dt>

**UnitId**
</dt> <dd>

Unité biométrique qui a généré l’exemple.

</dd> <dt>

**Identité**
</dt> <dd>

Structure [**d' \_ identité WINBIO**](winbio-identity.md) qui contient le GUID ou le SID de l’utilisateur qui fournit l’exemple biométrique.

</dd> <dt>

**Sous-fait**
</dt> <dd>

Valeur de sous- [**\_ \_ type biométrique WINBIO**](winbio-biometric-subtype-constants.md) qui spécifie le sous-facteur associé à un échantillon biométrique. le Windows Biometric Framework (WBF) prend actuellement en charge uniquement la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de sous-type.

-   WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle
-   WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger
-   \_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces

> [!IMPORTANT]
>
> N’essayez pas de valider la valeur fournie pour la valeur de sous- *fait* . le Service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation. Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valeur **ULong** qui contient des informations supplémentaires sur l’échec de capture d’un échantillon biométrique. Si la capture a réussi, ce paramètre a la valeur zéro. Les valeurs suivantes sont définies pour la capture d’empreinte digitale :

-   WINBIO \_ FP \_ trop \_ élevé
-   WINBIO \_ FP \_ trop \_ faible
-   WINBIO \_ FP \_ trop à \_ gauche
-   WINBIO \_ FP \_ trop à \_ droite
-   WINBIO \_ FP \_ trop \_ Fast
-   WINBIO \_ FP \_ trop \_ lent
-   \_ \_ qualité médiocre de WINBIO FP \_
-   WINBIO \_ FP \_ trop \_ incliné
-   WINBIO \_ FP \_ trop \_ petit
-   échec de la \_ fusion WINBIO FP \_ \_

</dd> </dl> </dd> <dt>

**Error**
</dt> <dd>

Structure qui identifie la réussite ou l’échec de l’opération surveillée.

<dl> <dt>

**ErrorCode**
</dt> <dd>

valeur **HRESULT** qui contient \_ un ou un code d’erreur qui résulte des calculs effectués par le Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

appelez la fonction [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) pour inscrire une routine de rappel afin de recevoir des notifications d’événements de la Windows Biometric Framework. Le rappel est une fonction personnalisée que vous devez définir pour votre application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





