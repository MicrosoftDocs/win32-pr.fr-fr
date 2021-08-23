---
title: Vérification des valeurs de retour IAccessible
description: Les développeurs clients ne doivent pas s’appuyer sur les macros COM (Component Object Model) ayant réussi et n’ont pas réussi à tester les valeurs de retour IAccessible, car les valeurs autres que \_ OK sont considérées comme ayant réussi.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1df43a316898ceeb751b114251ca8fbc91a8fc5360558a3929bcc3ecc47cce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759629"
---
# <a name="checking-iaccessible-return-values"></a>Vérification des valeurs de retour IAccessible

Les développeurs clients ne doivent pas s’appuyer sur les macros COM (Component Object Model) ayant [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) et [**n’ont pas**](/windows/desktop/api/winerror/nf-winerror-failed) réussi à tester les valeurs de retour [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , car les valeurs autres que \_ OK sont considérées comme ayant réussi. Par exemple, une méthode peut retourner \_ la valeur S false, qui est considérée comme un succès par la macro **Succeeded** , mais qui reçoit toujours un pointeur **null** dans un paramètre de sortie.

Les développeurs clients doivent se prémunir contre la possibilité que certains serveurs retournent des codes d’erreur autres que les valeurs documentées. Pour être sûr, vous devez vous assurer que tous les paramètres de sortie contiennent des informations valides et répondent aux critères suivants :

-   Tous les pointeurs ne sont pas **null**.
-   Le membre **VT** d’une structure [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) n’est pas égal à VT \_ vide.

 

 