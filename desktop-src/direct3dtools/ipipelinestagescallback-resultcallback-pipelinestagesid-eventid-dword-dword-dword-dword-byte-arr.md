---
description: Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b161dcfd67b4aabbfd77bc8bf07c927d22f85f66
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626106"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback :: ResultCallback, méthode

Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a>Paramètres

*stageId*   
Étape de pipeline représentée dans les résultats.

*Numéro*   
Événement représenté dans les résultats.

*Largeur*   
Largeur de l’image de visualisation du pipeline.

*celle*   
Hauteur de l’image de visualisation du pipeline.

*format*   
Format de l’image de visualisation du pipeline.

*corps*   
Taille de l’image en octets.

*\_mémoire tampon count5*   
Image de visualisation du pipeline.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
