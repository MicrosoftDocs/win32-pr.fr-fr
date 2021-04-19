---
description: Lors de l’utilisation de la directive INF RegisterDlls pour inscrire automatiquement des dll, les appelants de SetupInstallFromInfSection peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Message d’SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522429"
---
# <a name="spfilenotify_endregistration-message"></a>\_Message SPFILENOTIFY ENDREGISTRATION

Lors de l’utilisation de la directive INF **RegisterDlls** pour inscrire automatiquement des dll, les appelants de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit. Pour envoyer une **notification \_ ENDREGISTRATION SPFILENOTIFY** à une routine de rappel après avoir inscrit ou annulé l’inscription d’un fichier, incluez \_ le REGISTERCALLBACKAWARE de spinst plus l’ajout de la valeur de spinst \_ dans le paramètre *Flags* de **SetupInstallFromInfSection**. Pour envoyer une notification d’annulation de l’inscription, incluez le REGISTERCALLBACKAWARE de SPINst \_ plus \_ UNREGSVR de rotation dans le paramètre *Flags* .

La routine de rappel spécifiée par le paramètre *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) doit être le [type \_ \_ callback de fichier PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Définissez le paramètre de *contexte* sur le même *contexte* que celui spécifié dans **SetupInstallFromInfSection**. Définissez le paramètre de *notification* sur **SPFILENOTIFY \_ ENDREGISTRATION**.


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure d' [**\_ État de \_ contrôle \_ de Registre SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenant des informations sur le fichier en cours d’inscription ou non inscrit. Le membre **cbSize** doit être défini sur la taille de la structure. Le **nom** de fichier doit être défini sur le chemin d’accès complet du fichier en cours d’enregistrement. **Win32Error** doit être défini sur un [code d’erreur système](/windows/desktop/Debug/system-error-codes) indiquant un code d’erreur étendu. **FailureCode** doit être défini sur l’un des codes d’échec valides indiquant le résultat de l’inscription. Pour connaître les codes d’erreur valides, consultez [**\_ État du \_ contrôle \_ d’inscription SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Si le fichier est en cours d’enregistrement, *param2* doit être défini sur un pointeur désignant une valeur différente de zéro. Si l’inscription du fichier est annulée, la valeur de *param2* doit être un pointeur vers la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Après avoir reçu la notification, la fonction de rappel peut retourner l’une des valeurs suivantes.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | Arrêtez le traitement de la section INF.<br/>     |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Poursuivez le traitement de la section INF.<br/> |
| <dl> <dt>**ignorer le fichier \_**</dt> </dl>    | Continuer le traitement de la section INF<br/>  |



 

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

[**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)
</dt> </dl>

 

