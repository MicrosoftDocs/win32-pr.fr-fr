---
description: Les \_ constantes LINECALLFEATURE2 répertorient les fonctionnalités supplémentaires disponibles pour la Conférence, le transfert et les appels de parking.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b1ef95c5427c70455466fdc4e44424a8d7bc92f768698bd3356f28256b4dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003137"
---
# <a name="linecallfeature2_-constants"></a>\_Constantes LINECALLFEATURE2

Les constantes **LINECALLFEATURE2 \_** répertorient les fonctionnalités supplémentaires disponibles pour la Conférence, le transfert et les appels de parking.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité de « rappel » peut être appelée à l’aide de l' \_ option de rappel LINECOMPLMODE avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité « camp on » peut être appelée à l’aide de l' \_ option LINECOMPLMODE CAMPON avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité « intrus » peut être appelée à l’aide de l' \_ option LINECOMPLMODE intrusion avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité « conserver le message » peut être appelée à l’aide de l' \_ option de message LINECOMPLMODE avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Si ce bit est activé, une « aucune conférence débloquée » peut être créée à l’aide de l' \_ option LINECALLPARAMFLAGS NOHOLDCONFERENCE avec [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). Le \_ bit LINECALLFEATURE SETUPCONF est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Si ce bit est activé, vous pouvez créer un transfert en une étape à l’aide de l' \_ option LINECALLPARAMFLAGS ONESTEPTRANSFER avec [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Le \_ bit LINECALLFEATURE SETUPTRANSFER est également activé dans le membre **dwCallFeatures** .

> [!Note]  
> Si aucun des bits « compl ( » n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais \_ que LINECALLFEATURE COMPLETECALL est spécifié, il est possible que l’un d’eux fonctionne, alors que le fournisseur de services n’a pas spécifié quoi.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonction [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) peut être utilisée pour résoudre le transfert comme une conférence triple. Le \_ bit LINECALLFEATURE COMPLETETRANSF est également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonction [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) peut être utilisée pour résoudre le transfert comme un transfert normal. Le \_ bit LINECALLFEATURE COMPLETETRANSF est également activé dans le membre **dwCallFeatures** .

> [!Note]  
> Si ni TRANSFERNORM ni TRANSFERCONF n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais que LINECALLFEATURE \_ COMPLETETRANSF est spécifié, il est possible que soit fonctionne, mais que le fournisseur de services n’ait pas spécifié ce qui a été spécifié.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité de « stationnement dirigé » peut être appelée à l’aide de l' \_ option LINEPARKMODE dirigée avec [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Le \_ bit de parc LINECALLFEATURE sera également activé dans le membre **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Si ce bit est activé, la fonctionnalité « parc non dirigé » peut être appelée à l’aide de l' \_ option non directe LINEPARKMODE avec [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). Le \_ bit de parc LINECALLFEATURE sera également activé dans le membre **dwCallFeatures** .

> [!Note]  
> Si ni PARKDIRECT ni PARKNONDIRECT n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais \_ que LINECALLFEATURE Park est spécifié, il est possible que soit fonctionne, mais que le fournisseur de services n’ait pas spécifié ce qui a été spécifié.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




