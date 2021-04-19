---
description: Lors de l’utilisation de la directive INF RegisterDlls pour inscrire automatiquement des dll, les appelants de SetupInstallFromInfSection peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Message d’SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524365"
---
# <a name="spfilenotify_startregistration-message"></a>\_Message SPFILENOTIFY STARTREGISTRATION

Lors de l’utilisation de la directive INF **RegisterDlls** pour inscrire automatiquement des dll, les appelants de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit. Pour envoyer une notification **SPFILENOTIFY \_ STARTREGISTRATION** à la routine de rappel une fois avant d’inscrire un fichier, incluez le REGISTERCALLBACKAWARE de spinst plus la valeur de \_ l’argument spinst \_ dans le paramètre *Flags* de **SetupInstallFromInfSection**. Pour envoyer une notification d’annulation de l’inscription, incluez le REGISTERCALLBACKAWARE de SPINst \_ plus \_ UNREGSVR de rotation dans le paramètre *Flags* .

La routine de rappel spécifiée par le paramètre *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) doit être le [type \_ \_ callback de fichier PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Définissez le paramètre de *contexte* sur le même *contexte* que celui spécifié dans **SetupInstallFromInfSection**. Définissez le paramètre de *notification* sur **SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure d' [**\_ État de \_ contrôle \_ de Registre SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenant des informations sur le fichier en cours d’inscription ou non inscrit. Le membre **cbSize** doit être défini sur la taille de la structure. Le membre de **nom** de fichier doit être défini sur le chemin d’accès complet du fichier en cours d’enregistrement. **Win32Error** n’est pas utilisé et doit être défini sur aucune \_ erreur. **FailureCode** n’est pas utilisé et doit être défini sur SPREG \_ Success.

</dd> <dt>

*Param2* 
</dt> <dd>

Si le fichier est en cours d’enregistrement, *param2* doit être défini sur un pointeur désignant une valeur différente de zéro. Si l’inscription du fichier est annulée, la valeur de *param2* doit être un pointeur vers la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Après avoir reçu la notification, la fonction de rappel peut retourner l’une des valeurs suivantes.



| Code de retour                                                                                  | Description                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | N’enregistrez pas le fichier et ne l’annulez pas et arrêtez le traitement de la section INF.<br/>             |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Enregistrez ou annulez l’enregistrement du fichier et poursuivez le traitement de la section INF.<br/>                |
| <dl> <dt>**ignorer le fichier \_**</dt> </dl>    | Ignorer l’inscription ou annuler l’inscription du fichier, mais poursuivre le traitement de la section INF<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

