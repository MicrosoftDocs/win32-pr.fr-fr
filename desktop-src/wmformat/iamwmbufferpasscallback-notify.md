---
title: IAMWMBufferPassCallback méthode Notify
description: La méthode Notify est appelée par le code confidentiel pour chaque mémoire tampon qui est fournie pendant la diffusion en continu.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Méthode notifier le format Windows Media
- Méthode Notify Windows Media format, interface IAMWMBufferPassCallback
- Interface IAMWMBufferPassCallback Windows Media format, méthode Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102144"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback :: Notify, méthode

La méthode **Notify** est appelée par le code confidentiel pour chaque mémoire tampon qui est fournie pendant la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNSSBuffer3* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) exposée sur l’exemple de média.

</dd> <dt>

*pPin* \[ dans\]
</dt> <dd>

Pointeur vers le code confidentiel associé au flux multimédia auquel l’exemple appartient.

</dd> <dt>

*prtStart* \[ dans\]
</dt> <dd>

Heure de début de l’exemple.

</dd> <dt>

*prtEnd* \[ dans\]
</dt> <dd>

Heure de fin de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucune valeur de retour particulière n’est spécifiée. Le code PIN appelant ignore le **HRESULT**.

## <a name="remarks"></a>Notes

Cette méthode permet à une application d’examiner et d’agir sur les informations de la mémoire tampon du média avant le traitement du contenu de la mémoire tampon. L’application est chargée de connaître le type de média sur le code confidentiel. Ces informations peuvent être obtenues en obtenant d’abord les informations de flux à partir du profil, puis en appelant la méthode [**IConfigAsfWriter2 :: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) pour déterminer quel pin est associé à chaque flux.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Interface IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interface INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 