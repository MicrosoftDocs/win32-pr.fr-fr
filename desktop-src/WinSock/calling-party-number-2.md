---
description: Cette section répertorie la définition de type pour le numéro de tiers appelant.
ms.assetid: eb930123-28cf-4857-b7ad-f3c1786da7cc
title: Numéro du tiers appelant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b195c4c0f86dbe516d6487b0f3fc1b60958fd67ffbacc985f10f05ecf9822fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758469"
---
# <a name="calling-party-number"></a>Numéro du tiers appelant

Cette section répertorie la définition de type pour le numéro de tiers appelant.

``` syntax
#include <windows.h>

/* 
 *  values used for the Presentation_Indication field in 
 *  struct ATM_CALLING_PARTY_NUMBER_IE
 */
#define PI_ALLOWED                  0x00
#define PI_RESTRICTED               0x40
#define PI_NUMBER_NOT_AVAILABLE     0x80

/* 
 *  values used for the Screening_Indicator field in 
 *  struct ATM_CALLING_PARTY_NUMBER_IE
 */
#define SI_USER_NOT_SCREENED        0x00
#define SI_USER_PASSED              0x01
#define SI_USER_FAILED              0x02
#define SI_NETWORK                  0x03

typedef struct {
    ATM_ADDRESS ATM_Number;
    UCHAR       Presentation_Indication;
    UCHAR       Screening_Indicator;
} ATM_CALLING_PARTY_NUMBER_IE;
```

 

 



