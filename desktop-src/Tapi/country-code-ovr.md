---
description: Le code du pays ou de la région est pertinent uniquement lorsque le type d’adresse est LINEADDRESSTYPE \_ PHONENUMBER. Il identifie une zone du monde.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Code du pays ou de la région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013508"
---
# <a name="country-or-region-code"></a>Code du pays ou de la région

Le code du pays ou de la région est pertinent uniquement lorsque le type d’adresse est LINEADDRESSTYPE \_ PHONENUMBER. Il identifie une zone du monde.

Tous les fournisseurs de services qui prennent en charge l’utilisation de numéros de téléphone doivent prendre en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwCountryCode** de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CountryCode** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
