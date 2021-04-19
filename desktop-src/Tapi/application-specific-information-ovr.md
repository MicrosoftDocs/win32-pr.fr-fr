---
description: Les informations spécifiques à l’application permettent aux applications de transmettre les autres informations relatives à une session par le biais de l’interface TAPI. Ces informations ne sont pas interprétées par TAPI et l’utilisation est entièrement définie par les applications.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Informations spécifiques à l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531428"
---
# <a name="application-specific-information"></a>Informations spécifiques à l’application

Les informations spécifiques à l’application permettent aux applications de transmettre les autres informations relatives à une session par le biais de l’interface TAPI. Ces informations ne sont pas interprétées par TAPI et l’utilisation est entièrement définie par les applications.

Lorsque des informations spécifiques à l’application sont modifiées par une application, TAPI envoie à la session toutes les autres applications avec des privilèges d’analyse ou de propriétaire sur la session un événement indiquant qu’une modification s’est produite.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*DwAppSpecific* membre de *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**ligne \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* défini sur LINECALLINFOSTATE \_ APPSPECIFIC).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (membre **CIL \_ APPSPECIFIC** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
