---
description: Les informations de l’utilisateur sont une mémoire tampon qui peut être transmise d’une terminaison d’une connexion à une autre. Ces informations sont spécifiques à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Informations utilisateur-utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203b0b466d1b0b3f9da93cfefc5da737865da3cf5d40921dae6c969bfc9b9752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975289"
---
# <a name="user-user-information"></a>Informations utilisateur-utilisateur

Les informations de l’utilisateur sont une mémoire tampon qui peut être transmise d’une terminaison d’une connexion à une autre. Ces informations sont spécifiques à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** et **dwCallDataOffset** membres de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x : * *[**ITCallInfo :: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), appelé avec le membre **CIM \_ USERUSERINFO** de [**la \_ mémoire tampon CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo :: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
