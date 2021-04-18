---
description: Les \_ constantes LINECALLTREATMENT répertorient les traitements pour les appels qui ne sont pas répondus ou en attente. À l’exception de la validation des paramètres de base, le traitement des appels est un passage direct de l’interface TAPI au fournisseur de services.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528997"
---
# <a name="linecalltreatment_-constants"></a>\_Constantes LINECALLTREATMENT

Les constantes **LINECALLTREATMENT \_** répertorient les traitements pour les appels qui ne sont pas répondus ou en attente. À l’exception de la validation des paramètres de base, le traitement des appels est un passage direct de l’interface TAPI au fournisseur de services.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ occupé**
</dt> <dd> <dl> <dt>



Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend le signal occupé.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_musique LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend la musique.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**\_rappel LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend un signal de rappel.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**\_silence LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend le silence.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

La valeur 0x00000000 est réservée pour indiquer que le fournisseur de services ne prend pas en charge les traitements des appels. Les valeurs de la plage 0x00000005 à 0x000000FF sont réservées pour une définition ultérieure. Les valeurs de la plage 0x00000100 à 0xFFFFFFFF sont réservées à l’attribution par les fournisseurs de services et peuvent inclure l’identification de sélections musicales spécifiques ou d’annonces enregistrées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




