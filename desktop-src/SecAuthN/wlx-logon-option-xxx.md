---
description: Les valeurs sont utilisées par le paramètre dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096158"
---
# <a name="wlx_logon_option_xxx"></a>\_option de connexion wlx \_ \_ xxx

\[l' \_ \_ OPTION de connexion WLX \_ XXX constante n’est plus disponible pour une utilisation à partir de Windows Server 2008 et Windows Vista.\]

Les valeurs de l' **\_ option de connexion wlx \_ \_ xxx** sont utilisées par le paramètre *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 

Une fois la connexion établie, votre DLL GINA peut utiliser cette valeur pour spécifier l’option suivante.



| Constante                                                                                                                                                                                          | Description                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**\_profil d’accès d’ouverture de session wlx \_ \_ \_**</dt> </dl> | Spécifie que Winlogon ne doit pas charger de profil pour l’utilisateur connecté. Dans ce cas, soit votre DLL GINA chargera le profil, soit l’utilisateur n’a pas besoin d’un profil.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                               |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 




