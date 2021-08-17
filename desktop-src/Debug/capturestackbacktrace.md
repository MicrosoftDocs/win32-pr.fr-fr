---
UID: ''
title: CaptureStackBackTrace fonction)
description: Capture une trace arrière de la pile en parcourant la pile.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279500"
---
# <a name="capturestackbacktrace-function"></a>CaptureStackBackTrace fonction)

## <a name="description"></a>Description

Capture une trace arrière de la pile en parcourant la pile et en enregistrant les informations pour chaque frame.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Paramètres

### <a name="framestoskip-in"></a>FramesToSkip [in]

Nombre de frames à ignorer à partir du début de la trace arrière.

### <a name="framestocapture-in"></a>FramesToCapture [in]

Nombre de frames à capturer.
Vous pouvez capturer jusqu’à **MAXUSHORT** frames.

**Windows Server 2003 et Windows XP :**  La somme des paramètres *FramesToSkip* et *FramesToCapture* doit être inférieure à 63.

### <a name="backtrace-out"></a>Traces [out]

Tableau de pointeurs capturés à partir de la trace de la pile actuelle.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, optional]

Valeur qui peut être utilisée pour organiser des tables de hachage.
Si ce paramètre a la valeur **null**, aucune valeur de hachage n’est calculée.

Cette valeur est calculée en fonction des valeurs des pointeurs retournés dans le tableau de suivi des traces.
Deux traces de pile identiques génèrent des valeurs de hachage identiques.

## <a name="returns"></a>Retours

Nombre de frames capturés.

## <a name="remarks"></a>Remarques

la fonction **CaptureStackBackTrace** est définie en tant que fonction **RtlCaptureStackBackTrace** (la définition est incluse dans le SDK Windows à partir de Windows Vista).
Pour plus d’informations, consultez WinBase. h et Winnt. h.

## <a name="see-also"></a>Voir aussi
