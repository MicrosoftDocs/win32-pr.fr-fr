---
description: Énumération utilisée pour indiquer le type d’un événement.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: EVENTTYPE, énumération
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: daa61cc8358fb0dc59f4b819e27077c68748b995
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624435"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>EVENTTYPE, énumération

Énumération utilisée pour indiquer le type d’un événement.

## <a name="syntax"></a>Syntax

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a>Constantes

<span id="ET_NONE"></span><span id="et_none"></span>**ET \_ aucun**  
Valeur qui correspond à aucun événement.

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET \_ SESSIONSTART**  
Valeur qui correspond à un événement de démarrage de session.

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET \_ SESSIONEND**  
Valeur qui correspond à un événement de fin de session.

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET \_ PROCESSSTART**  
Valeur qui correspond à un événement de démarrage de processus.

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET \_ PROCESSEND**  
Valeur qui correspond à un événement de fin de processus.

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET \_ FRAMEBEGIN**  
Valeur qui correspond à un événement de début de frame.

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET \_ FRAMEEND**  
Valeur qui correspond à un événement de fin de cadre. Non utilisé.

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ USEREVENTBEGIN**  
Valeur qui correspond à un événement de début d’événement utilisateur.

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ USEREVENTEND**  
Valeur qui correspond à un événement de fin d’événement utilisateur. Non utilisé.

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET \_ USERMARKER**  
Valeur qui correspond à un événement de marqueur utilisateur.

<span id="ET_CALL"></span><span id="et_call"></span>**\_appel et**  
Valeur qui correspond à un événement d’appel.

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ OBJECTCREATION**  
Valeur qui correspond à un événement de création d’objet.

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ OBJECTPOPULATION**  
Valeur qui correspond à un événement de remplissage d’objet.

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ CALLSYNC**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**ET \_ dessin**  
Valeur qui correspond à un événement d’appel de dessin.

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET \_ Dispatch**  
Valeur qui correspond à un événement de dispatch.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>
