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
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847534"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback :: Notify, méthode

La méthode **Notify** est appelée par le code confidentiel pour chaque mémoire tampon qui est fournie pendant la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
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

## <a name="remarks"></a>Remarques

Cette méthode permet à une application d’examiner et d’agir sur les informations de la mémoire tampon du média avant le traitement du contenu de la mémoire tampon. L’application est chargée de connaître le type de média sur le code confidentiel. Ces informations peuvent être obtenues en obtenant d’abord les informations de flux à partir du profil, puis en appelant la méthode [**IConfigAsfWriter2 :: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) pour déterminer quel pin est associé à chaque flux.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DirectShow Référence QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Interface IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interface INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 