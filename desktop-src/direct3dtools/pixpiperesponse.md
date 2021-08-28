---
description: Énumération utilisée pour envoyer des réponses du moteur de capture à Graphics Diagnostics.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631687"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Énumération PixPipeResponse

Énumération utilisée pour envoyer des réponses du moteur de capture à Graphics Diagnostics.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NOUVELLES \_ données \_ disponibles**  
Réponse qui indique que les nouvelles données ont été écrites dans le journal de graphisme et sont prêtes à être lues.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**données d’EXPÉRIMENTation \_**  
Réponse qui indique les informations de configuration relatives à la session de capture.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Réponse indiquant que le moteur de capture a rencontré une erreur.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Réponse qui indique que le moteur de capture a démarré la capture des informations graphiques. Cela ne signifie pas que les données sont disponibles pour être examinées pour l’instant.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**données PARTIELles \_**  
Réponse qui indique que des données partielles ont été écrites dans le journal de graphisme.

<span id="READY"></span><span id="ready"></span>**MONDIALISABLES**  
Réponse qui indique que le moteur de capture est prêt à capturer les informations graphiques.

<span id="DONE"></span><span id="done"></span>**CAS**  
Interne

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Réponse qui indique qu’une capture de frame a démarré.

<span id="STATUS"></span><span id="status"></span>**STATU**  
Réponse qui indique des informations d’État sur l’application capturée ; par exemple, cadence.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



