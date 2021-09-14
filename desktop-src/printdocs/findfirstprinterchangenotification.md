---
description: La fonction FindFirstPrinterChangeNotification crée un objet de notification de modification et retourne un handle à l’objet. Vous pouvez ensuite utiliser ce handle dans un appel à l’une des fonctions Wait pour surveiller les modifications apportées à l’imprimante ou au serveur d’impression.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: FindFirstPrinterChangeNotification, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235601"
---
# <a name="findfirstprinterchangenotification-function"></a>FindFirstPrinterChangeNotification fonction)

La fonction **FindFirstPrinterChangeNotification** crée un objet de notification de modification et retourne un handle à l’objet. Vous pouvez ensuite utiliser ce handle dans un appel à l’une des fonctions Wait pour surveiller les modifications apportées à l’imprimante ou au serveur d’impression.

L’appel **FindFirstPrinterChangeNotification** spécifie le type de modifications à surveiller. Vous pouvez spécifier un ensemble de conditions pour surveiller les modifications, un ensemble de champs d’informations d’imprimante à surveiller, ou les deux.

Une opération d’attente sur le handle de notification de modification est effectuée lorsque l’une des modifications spécifiées se produit sur l’imprimante ou le serveur d’impression spécifié. Vous appelez ensuite la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) pour récupérer des informations sur la modification et réinitialiser l’objet de notification de modification pour l’utiliser lors de l’opération d’attente suivante.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante ou le serveur d’impression que vous souhaitez analyser. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*fdwFilter* 
</dt> <dd>

Conditions qui obligeront l’objet de notification de modification à entrer dans un état signalé. Une notification de modification se produit lorsqu’une ou plusieurs des conditions spécifiées sont remplies. Le paramètre *fdwFilter* peut être égal à zéro si *pPrinterNotifyOptions* n’est pas **null**.

Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**\_formulaire de modification de l’imprimante \_**</dt> </dl>                                   | Notifier toute modification apportée à un formulaire. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants :<br/> <dl> <dd>\_Ajouter un \_ \_ formulaire de modification d’imprimante</dd> <dd>\_formulaire de modification de l’imprimante \_ \_</dd> <dd>\_formulaire de \_ Suppression de modification d’imprimante \_</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**\_travail de modification d’imprimante \_**</dt> </dl>                                      | Notifier toute modification apportée à un travail. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants :<br/> <dl> <dd>changement d’imprimante \_ \_ Ajouter un \_ travail</dd> <dd>\_travail d' \_ ensemble de modifications d’imprimante \_</dd> <dd>\_tâche de \_ Suppression de modification d’imprimante \_</dd> <dd>\_travail d' \_ écriture de modification d’imprimante \_</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**\_port de modification de l’imprimante \_**</dt> </dl>                                   | Notifier toute modification apportée à un port. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants :<br/> <dl> <dd>changement d’imprimante \_ \_ Ajouter un \_ port</dd> <dd>\_modifier le \_ port de configuration de l’imprimante \_ </dd> <dd>\_port de \_ Suppression de modification d’imprimante \_</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**changement d’imprimante du \_ \_ processeur d’impression \_**</dt> </dl> | Notifier toute modification apportée à un processeur d’impression. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants : <br/> <dl> <dd>modification de l’imprimante \_ \_ Ajouter un \_ processeur d’impression \_ </dd> <dd>changement d’imprimante- \_ \_ supprimer le \_ processeur d’impression \_</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**imprimante de changement d’imprimante \_ \_**</dt> </dl>                          | Notifier toute modification apportée à une imprimante. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants :<br/> <dl> <dd>modification de l’imprimante \_ \_ Ajouter l' \_ imprimante</dd> <dd>imprimante de \_ jeu de modifications d’imprimante \_ \_</dd> <dd>modification de l’imprimante \_ \_ Supprimer l' \_ imprimante</dd> <dd>\_ \_ imprimante échec de \_ la modification de l’imprimante \_</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**IMPRIMANTE \_ changer \_ le \_ pilote d’imprimante**</dt> </dl>    | Notifier toute modification apportée à un pilote d’imprimante. Vous pouvez définir cet indicateur général ou un ou plusieurs des indicateurs spécifiques suivants :<br/> <dl> <dd>changement d’imprimante \_ \_ Ajouter un \_ pilote d’imprimante \_</dd> <dd>\_pilote d' \_ imprimante de jeu de modifications d’imprimante \_ \_</dd> <dd>modification de l’imprimante \_ \_ supprimer le \_ pilote d’imprimante \_</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**\_tout modifier l’imprimante \_**</dt> </dl>                                      | Notifiez si l’une des modifications précédentes se produit.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_serveur de changement d’imprimante \_**</dt> </dl>                             | Windows 7 : notification de toute modification apportée au serveur.<br/> Cet indicateur n’est pas inclus dans les modifications contrôlées en définissant la valeur de **\_ \_ modifier l’imprimante** .<br/>                                                                                                                                                                                                      |



 

Pour obtenir une description des indicateurs plus spécifiques dans le tableau précédent, consultez la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .

</dd> <dt>

*fdwOptions* 
</dt> <dd>

Indicateur qui détermine la catégorie des imprimantes pour lesquelles les notifications fonctionnent.



| Valeur                                                                                                                                                                                                                                                               | Signification                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**Imprimante \_ NOTIFIer la \_ catégorie \_ tous les**</dt> <dt>0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retourne des notifications pour les imprimantes 2D et 3D.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**Imprimante \_ NOTIFIer la \_ catégorie 0x002000 \_ 3D**</dt> <dt></dt> </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retourne uniquement les notifications pour les imprimantes 3D.<br/>        |



 

Lorsque cet indicateur est défini sur zéro (0), **FindFirstPrinterChangeNotification** ne fonctionne que pour les imprimantes 2D. Il s’agit de la valeur par défaut.

</dd> <dt>

*pPrinterNotifyOptions* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ options de notification d’imprimante**](printer-notify-options.md) . Le membre **pTypes** de cette structure est un tableau d’une ou de plusieurs structures de types d’options de notification d' [**imprimante \_ \_ \_**](printer-notify-options-type.md) , chacune d’elles spécifiant un champ d’informations sur l’imprimante à surveiller. Une notification de modification se produit lorsqu’un ou plusieurs des champs spécifiés sont modifiés. Lorsqu’une modification se produit, la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) peut récupérer les nouvelles informations sur l’imprimante. Ce paramètre peut avoir la **valeur null** si *fdwFilter* est différent de zéro.

Pour obtenir la liste des champs qui peuvent être analysés, voir [**Printer \_ Notify \_ options \_ type**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est un handle vers un objet de notification de modification associé à l’imprimante ou au serveur d’impression spécifié.

Si la fonction échoue, la valeur de retour est une valeur de handle non valide \_ \_ .

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Pour surveiller une imprimante ou un serveur d’impression, appelez la fonction **FindFirstPrinterChangeNotification** , puis utilisez le descripteur d’objet de notification de modification retourné dans un appel à l’une des [fonctions Wait](/windows/desktop/Sync/wait-functions). Une opération d’attente sur un objet de notification de modification est satisfaite lorsque l’objet de notification de modification passe à l’état signalé. Le système signale l’objet lorsqu’une ou plusieurs des modifications spécifiées par *fdwFilter* ou *pPrinterNotifyOptions* se produisent sur l’imprimante ou le serveur d’impression analysé.

Lorsque vous appelez **FindFirstPrinterChangeNotification**, *fdwFilter* doit être différent de zéro ou *pPrinterNotifyOptions* doit avoir une **valeur non null**. Si les deux sont spécifiés, des notifications sont générées pour les deux.

Quand une opération d’attente sur un objet de notification de modification d’imprimante est satisfaite, appelez la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) pour déterminer la cause de la notification. Pour une condition spécifiée par *fdwFilter*, **FindNextPrinterChangeNotification** signale la ou les conditions qui ont changé. Pour un champ d’informations d’imprimante spécifié par *pPrinterNotifyOptions*, **FindNextPrinterChangeNotification** signale le ou les champs qui ont changé, ainsi que les nouvelles informations pour ces champs. **FindNextPrinterChangeNotification** réinitialise également l’objet de notification de modification à l’état non signalé afin que vous puissiez l’utiliser dans une autre opération d’attente pour continuer à surveiller l’imprimante ou le serveur d’impression.

À une exception près, n’appelez pas la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) si l’objet de notification de modification n’est pas dans l’état signalé. Si la fonction Wait retourne le délai d’attente de la valeur \_ , l’objet de modification n’est pas dans l’état signalé. Appelez la fonction **FindNextPrinterChangeNotification** uniquement si la fonction Wait est réussie sans dépassement du délai d’attente. L’exception est quand **FindNextPrinterChangeNotification** est appelé avec le \_ bit d' \_ actualisation des options \_ de notification d’imprimante défini dans le paramètre *pPrinterNotifyOptions* .

Lorsque vous n’avez plus besoin de l’objet de notification de modification, fermez-le en appelant la fonction [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

Les appelants de **FindFirstPrinterChangeNotification** doivent s’assurer que le handle d’imprimante passé dans **FindFirstPrinterChangeNotification** reste valide jusqu’à ce que [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) soit appelé. Si le descripteur d’imprimante est fermé avant le handle de notification de modification d’imprimante, les notifications supplémentaires ne seront pas remises.

**FindFirstPrinterChangeNotification** n’enverra pas de notifications de modifications pour les imprimantes 3D aux descripteurs de serveur.

> [!Note]  
> dans Windows XP avec Service Pack 2 (SP2) et versions ultérieures, le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes peut être activée. Si un utilisateur établit une connexion d’imprimante avec un autre ordinateur et que l’exception n’est pas activée, l’utilisateur ne reçoit pas de notifications de modification d’imprimante à partir du serveur. Un administrateur d’ordinateur devra activer l’exception.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_options de notification d’imprimante \_**](printer-notify-options.md)
</dt> <dt>

[**\_type d' \_ options de notification d’imprimante \_**](printer-notify-options-type.md)
</dt> </dl>

 

