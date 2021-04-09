---
description: La fonction FindNextPrinterChangeNotification récupère des informations sur la notification de modification la plus récente pour un objet de notification de modification associé à une imprimante ou à un serveur d’impression.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: FindNextPrinterChangeNotification, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866181"
---
# <a name="findnextprinterchangenotification-function"></a>FindNextPrinterChangeNotification fonction)

La fonction **FindNextPrinterChangeNotification** récupère des informations sur la notification de modification la plus récente pour un objet de notification de modification associé à une imprimante ou à un serveur d’impression. Appelez cette fonction quand une opération d’attente sur l’objet de notification de modification est satisfaite.

La fonction réinitialise également l’objet de notification de modification à l’état non signalé. Vous pouvez ensuite utiliser l’objet dans une autre opération d’attente pour continuer à surveiller l’imprimante ou le serveur d’impression. Le système d’exploitation affecte à l’objet l’état signalé la prochaine fois qu’un jeu de modifications spécifié se produit sur l’imprimante ou le serveur d’impression. La fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crée l’objet de notification de modification et spécifie l’ensemble de modifications à surveiller.

## <a name="syntax"></a>Syntaxe


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hChange* \[ dans\]
</dt> <dd>

Handle d’un objet de notification de modification associé à une imprimante ou à un serveur d’impression. Vous obtenez ce type de handle en appelant la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Le système d’exploitation définit cet objet de notification de modification à l’état signalé lorsqu’il détecte l’une des modifications spécifiées dans le filtre de notification de modification de l’objet.

</dd> <dt>

*pdwChange* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable dont les bits sont définis pour indiquer les modifications qui se sont produites pour provoquer la notification la plus récente. Les indicateurs de bits qui peuvent être définis correspondent à ceux spécifiés dans le paramètre *fdwFilter* de l’appel [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Le système définit un ou plusieurs des indicateurs binaires suivants.



| Valeur                                                                                                                                                                                                                                             | Signification                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**\_Ajouter un \_ \_ formulaire de modification d’imprimante**</dt> </dl>                                                     | Un formulaire a été ajouté au serveur.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**changement d’imprimante \_ \_ Ajouter un \_ travail**</dt> </dl>                                                        | Un travail d’impression a été envoyé à l’imprimante.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**changement d’imprimante \_ \_ Ajouter un \_ port**</dt> </dl>                                                     | Un port ou une analyse a été ajouté au serveur.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**modification de l’imprimante \_ \_ Ajouter un \_ processeur d’impression \_**</dt> </dl>                   | Un processeur d’impression a été ajouté au serveur.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**modification de l’imprimante \_ \_ Ajouter l' \_ imprimante**</dt> </dl>                                            | Une imprimante a été ajoutée au serveur.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**changement d’imprimante \_ \_ Ajouter un \_ pilote d’imprimante \_**</dt> </dl>                      | Un pilote d’imprimante a été ajouté au serveur.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**\_modifier le \_ port de configuration de l’imprimante \_**</dt> </dl>                                   | Un port a été configuré sur le serveur.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**\_formulaire de \_ Suppression de modification d’imprimante \_**</dt> </dl>                                            | Un formulaire a été supprimé du serveur.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**\_tâche de \_ Suppression de modification d’imprimante \_**</dt> </dl>                                               | Un travail a été supprimé.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**\_port de \_ Suppression de modification d’imprimante \_**</dt> </dl>                                            | Un port ou une analyse a été supprimé du serveur.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**changement d’imprimante- \_ \_ supprimer le \_ processeur d’impression \_**</dt> </dl>          | Un processeur d’impression a été supprimé du serveur.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**modification de l’imprimante \_ \_ Supprimer l' \_ imprimante**</dt> </dl>                                   | Une imprimante a été supprimée.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**modification de l’imprimante \_ \_ supprimer le \_ pilote d’imprimante \_**</dt> </dl>             | Un pilote d’imprimante a été supprimé du serveur.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**\_ \_ imprimante échec de \_ la modification de l’imprimante \_**</dt> </dl> | Une connexion d’imprimante a échoué.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**\_formulaire de modification de l’imprimante \_ \_**</dt> </dl>                                                     | Un formulaire a été défini sur le serveur.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**\_travail d' \_ ensemble de modifications d’imprimante \_**</dt> </dl>                                                        | Un travail a été défini.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**imprimante de \_ jeu de modifications d’imprimante \_ \_**</dt> </dl>                                            | Une imprimante a été définie.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**\_pilote d' \_ imprimante de jeu de modifications d’imprimante \_ \_**</dt> </dl>                      | Un pilote d’imprimante a été défini.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_travail d' \_ écriture de modification d’imprimante \_**</dt> </dl>                                                  | Les données du travail ont été écrites.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**\_délai de modification de l’imprimante \_**</dt> </dl>                                                         | Le travail a expiré.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_serveur de changement d’imprimante \_**</dt> </dl>                                                            | Windows 7 : une modification s’est produite sur le serveur.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ options de notification d’imprimante**](printer-notify-options.md) . Définissez le membre **Flags** de cette structure **sur \_ options Notify d’imprimante \_ \_ Actualiser** pour que la fonction retourne les données actuelles pour tous les champs d’informations d’imprimante analysés. La fonction ignore tous les autres membres de la structure. Ce paramètre peut être **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable pointeur qui reçoit un pointeur vers une mémoire tampon en lecture seule allouée par le système. Appelez la fonction [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) pour libérer la mémoire tampon lorsque vous n’en avez plus besoin. Ce paramètre peut avoir la **valeur null** si aucune information n’est requise.

La mémoire tampon contient une structure d' [**\_ \_ informations de notification d’imprimante**](printer-notify-info.md) , qui contient un tableau de structures de [**\_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) . Chaque élément du tableau contient des informations sur l’un des champs spécifiés dans le paramètre *pPrinterNotifyOptions* de l’appel [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . En règle générale, la fonction fournit uniquement des données pour les champs qui ont été modifiés pour provoquer la notification la plus récente. Toutefois, si la structure vers laquelle pointe le paramètre *pPrinterNotifyOptions* spécifie l’actualisation des options de notification d' **imprimante \_ \_ \_**, la fonction fournit des données pour tous les champs surveillés.

Si le bit d' **informations de notification d’imprimante \_ \_ \_ rejeté** est défini dans le membre **Flags** de la structure d' [**informations de \_ notification \_ d’imprimante**](printer-notify-info.md) , un dépassement de capacité ou une erreur se sont produits et des notifications ont peut-être été perdues. Dans ce cas, aucune notification supplémentaire n’est envoyée tant que vous n’avez pas effectué un deuxième appel **FindNextPrinterChangeNotification** qui spécifie l' **\_ \_ \_ actualisation des options Notify** de l’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Appelez la fonction **FindNextPrinterChangeNotification** après la satisfaction d’une opération d’attente sur un objet de notification créé par [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . L’appel de **FindNextPrinterChangeNotification** vous permet d’obtenir des informations sur la modification qui a respecté l’opération d’attente et réinitialise l’objet de notification afin qu’il puisse être signalé lorsque la modification suivante se produit.

À une exception près, n’appelez pas la fonction **FindNextPrinterChangeNotification** si l’objet de notification de modification n’est pas dans l’état signalé. Si une fonction Wait retourne le **\_ délai d'** attente de la valeur, l’objet de modification n’est pas dans l’état signalé. Appelez la fonction **FindNextPrinterChangeNotification** uniquement si la fonction Wait est réussie sans dépassement du délai d’attente. L’exception est quand **FindNextPrinterChangeNotification** est appelé avec le bit d’actualisation des options de notification d’imprimante défini dans le paramètre *pPrinterNotifyOptions* . **\_ \_ \_** Notez que même lorsque cet indicateur est défini, il est toujours possible de définir l’indicateur d’informations de notification d’imprimante dans le paramètre *ppPrinterNotifyInfo* . **\_ \_ \_**

Pour continuer à surveiller les modifications apportées à l’imprimante ou au serveur d’impression, répétez le cycle de l’appel de l’une des [fonctions d’attente](/windows/desktop/Sync/wait-functions) , puis appelez la fonction **FindNextPrinterChangeNotification** pour examiner la modification et réinitialiser l’objet de notification.

**FindNextPrinterChangeNotification** peut combiner plusieurs modifications apportées au même champ d’informations d’imprimante en une seule notification. Dans ce cas, la fonction réduit généralement toutes les modifications apportées au champ en une seule entrée dans le tableau des structures de [**données d’informations de notification d’imprimante \_ \_ \_**](printer-notify-info-data.md) dans *ppPrinterNotifyInfo*; l’entrée unique signale uniquement les informations les plus récentes. Toutefois, pour certains champs d’informations sur les travaux et les imprimantes, la fonction peut retourner plusieurs entrées de tableau pour le même champ. Dans ce cas, la dernière entrée de tableau pour le champ signale les données actuelles, et les entrées précédentes contiennent les données pour les étapes intermédiaires.

Lorsque vous n’avez plus besoin de l’objet de notification de modification, fermez-le en appelant la fonction [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

> [!Note]  
> Dans Windows XP avec Service Pack 2 (SP2) et versions ultérieures, le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes peut être activée. Si un utilisateur établit une connexion d’imprimante avec un autre ordinateur et que l’exception n’est pas activée, l’utilisateur ne reçoit pas de notifications de modification d’imprimante à partir du serveur. Un administrateur d’ordinateur devra activer l’exception.

 

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre la façon dont vous pouvez surveiller l’état de l’imprimante à l’aide de ces fonctions.


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a>Configuration requise



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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_informations de notification de l’imprimante \_**](printer-notify-info.md)
</dt> <dt>

[**\_données d' \_ informations de notification d’imprimante \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_options de notification d’imprimante \_**](printer-notify-options.md)
</dt> </dl>

 

