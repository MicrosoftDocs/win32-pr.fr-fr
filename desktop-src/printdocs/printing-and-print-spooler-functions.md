---
description: L’API spouleur d’impression contient les fonctions et les structures de données utilisées par les applications pour gérer le spouleur d’impression Windows, ainsi que les imprimantes et les travaux d’impression qu’il contrôle.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Fonctions API du spouleur d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210353"
---
# <a name="print-spooler-api-functions"></a>Fonctions API du spouleur d’impression

L’API spouleur d’impression contient les fonctions et les structures de données utilisées par les applications pour gérer le spouleur d’impression Windows, ainsi que les imprimantes et les travaux d’impression qu’il contrôle.

Les fonctions de l’API du spouleur d’impression sont réparties dans les groupes suivants :

-   [Fonctions du travail d’impression](#print-job-functions)
-   [Fonctions de l’interface utilisateur de l’imprimante](#printer-user-interface-functions)
-   [Fonctions d’imprimante](#printer-functions)
-   [Fonctions de notification de modification d’imprimante](#printer-change-notification-functions)
-   [Fonctions de formulaire d’imprimante](#printer-form-functions)
-   [Fonctions du spouleur d’impression](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Fonctions du travail d’impression

Ces fonctions envoient des travaux d’impression à une imprimante et suivent et contrôlent les travaux d’impression dans le spouleur d’impression.



| Fonction                                                                      | Description                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | La fonction [**AddJob**](/windows/desktop/printdocs/addjob) ajoute un travail d’impression à la liste des travaux d’impression qui peuvent être planifiés par le spouleur d’impression. La fonction récupère le nom du fichier que vous pouvez utiliser pour stocker le travail. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | La fonction [**ClosePrinter**](/windows/desktop/printdocs/closeprinter) ferme l’objet Printer spécifié. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | La fonction [**DocumentEvent**](/windows/desktop/printdocs/documentevent) est un gestionnaire d’événements pour les événements associés à l’impression d’un document. <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | La fonction [**DocumentProperties**](/windows/desktop/printdocs/documentproperties) récupère ou modifie les informations d’initialisation de l’imprimante ou affiche une feuille de propriétés de configuration de l’imprimante pour l’imprimante spécifiée. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | La fonction [**EndDocPrinter**](/windows/desktop/printdocs/enddocprinter) met fin à un travail d’impression pour l’imprimante spécifiée. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | La fonction [**EndPagePrinter**](/windows/desktop/printdocs/endpageprinter) informe le spouleur d’impression que l’application se trouve à la fin d’une page dans un travail d’impression. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | La fonction [**EnumJobs**](/windows/desktop/printdocs/enumjobs) récupère des informations sur un ensemble spécifié de travaux d’impression pour une imprimante spécifiée. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | La fonction [**GetJob**](/windows/desktop/printdocs/getjob) récupère des informations sur un travail d’impression spécifié. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | La fonction [**OpenPrinter**](/windows/desktop/printdocs/openprinter) récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Récupère un handle vers l’imprimante, le serveur d’impression ou d’autres types de handles spécifiés dans le sous-système d’impression, tout en définissant certaines options d’imprimante.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Signale au service spouleur d’impression si un travail d’impression XPS se trouve dans la phase de mise en file d’attente ou de rendu et quelle partie du traitement est actuellement en cours.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | La fonction [**ScheduleJob**](/windows/desktop/printdocs/schedulejob) demande que le spouleur d’impression planifie l’impression d’un travail d’impression spécifié. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | La fonction [**SetJob**](/windows/desktop/printdocs/setjob) suspend, reprend, annule ou redémarre un travail d’impression sur une imprimante spécifiée. Vous pouvez également utiliser la fonction **SetJob** pour définir les paramètres du travail d’impression, tels que la priorité du travail d’impression et le nom du document. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | La fonction [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) informe le spouleur d’impression qu’un document doit être mis en file d’attente pour l’impression. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | La fonction [**StartPagePrinter**](/windows/desktop/printdocs/startpageprinter) informe le spouleur qu’une page va être imprimée sur l’imprimante spécifiée. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Fonctions de l’interface utilisateur de l’imprimante

Ces fonctions affichent une interface utilisateur qui permet à l’utilisateur de sélectionner ou de configurer une imprimante.



| Fonction                                                                    | Description                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | La fonction [**AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties) affiche une boîte de dialogue de configuration de l’imprimante pour l’imprimante spécifiée, ce qui permet à l’utilisateur de configurer cette imprimante. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | La fonction [**ConfigurePort**](/windows/desktop/printdocs/configureport) affiche la boîte de dialogue de configuration du port pour un port sur le serveur spécifié. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | La fonction [**ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg) affiche une boîte de dialogue qui permet aux utilisateurs de parcourir les imprimantes et de s’y connecter sur un réseau. Si l’utilisateur sélectionne une imprimante, la fonction tente de créer une connexion à celle-ci ; Si aucun pilote approprié n’est installé sur le serveur, l’utilisateur a la possibilité de créer une imprimante localement. <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | La fonction [**PrinterProperties**](/windows/desktop/printdocs/printerproperties) affiche une feuille de propriétés Printer-Properties pour l’imprimante spécifiée. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Fonctions d’imprimante

Ces fonctions ajoutent et configurent les imprimantes que le spouleur d’impression utilise.



| Fonction                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | La fonction [**AbortPrinter**](/windows/desktop/printdocs/abortprinter) supprime le fichier de mise en file d’attente de l’imprimante si celle-ci est configurée pour la mise en file d’attente. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter**](addprinter.md)<br/>                           | La fonction [**AddPrinter**](/windows/desktop/printdocs/addprinter) ajoute une imprimante à la liste des imprimantes prises en charge pour un serveur spécifié. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | La fonction **AddPrinterConnection** ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel et spécifie les détails de connexion.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | La fonction [**DeletePrinter**](/windows/desktop/printdocs/deleteprinter) supprime l’objet Printer spécifié. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | La fonction [**DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection) supprime une connexion à une imprimante qui a été établie par un appel à [**AddPrinterConnection**](addprinterconnection.md) ou [**ConnectToPrinterDlg**](connecttoprinterdlg.md). <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | La fonction [**DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata) supprime les données de configuration spécifiées pour une imprimante. Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées. La fonction **DeletePrinterData** supprime l’une de ces valeurs, spécifiée par son nom de valeur. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | La fonction [**DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex) supprime une valeur spécifiée des données de configuration pour une imprimante. Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées stockées dans une hiérarchie de clés de registre. La fonction supprime une valeur spécifiée sous une clé spécifiée. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | La fonction [**DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey) supprime une clé spécifiée et toutes ses sous-clés pour une imprimante spécifiée. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | La fonction [**EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata) énumère les données de configuration d’une imprimante spécifiée. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | La fonction [**EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex) énumère tous les noms de valeur et les données pour une imprimante et une clé spécifiées. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | La fonction [**EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey) énumère les sous-clés d’une clé spécifiée pour une imprimante spécifiée. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | La fonction [**EnumPrinters**](/windows/desktop/printdocs/enumprinters) énumère les imprimantes disponibles, les serveurs d’impression, les domaines ou les fournisseurs d’impression. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | La fonction [**FlushPrinter**](/windows/desktop/printdocs/flushprinter) envoie une mémoire tampon à l’imprimante afin de l’effacer d’un état transitoire. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | La fonction [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) récupère le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | La fonction [**GetPrinter**](/windows/desktop/printdocs/getprinter) récupère des informations sur une imprimante spécifiée. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | La fonction [**GetPrinterData**](/windows/desktop/printdocs/getprinterdata) récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | La fonction [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié. **GetPrinterDataEx** peut récupérer des valeurs stockées par la fonction [**SetPrinterData**](setprinterdata.md) . En outre, **GetPrinterDataEx** peut récupérer des valeurs stockées sous une clé spécifiée par la fonction [**SetPrinterDataEx**](setprinterdataex.md) . <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | La fonction [**IsValidDevmode**](isvaliddevmode.md) vérifie que le contenu d’une structure DEVMODE est valide. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | La fonction [**ReadPrinter**](/windows/desktop/printdocs/readprinter) récupère les données de l’imprimante spécifiée. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | La fonction [**ResetPrinter**](/windows/desktop/printdocs/resetprinter) spécifie les valeurs du type de données et du mode de l’appareil à utiliser pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) . Ces valeurs peuvent être remplacées à l’aide de la fonction [**SetJob**](setjob.md) après le début de l’impression du document. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | La fonction [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) définit le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | La fonction [**SetPort**](/windows/desktop/printdocs/setport) définit l’état associé à un port d’imprimante. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | La fonction [**SetPrinter**](/windows/desktop/printdocs/setprinter) définit les données pour une imprimante spécifiée ou définit l’état de l’imprimante spécifiée en interrompant l’impression, en reprenant l’impression ou en effaçant tous les travaux d’impression. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | La fonction [**SetPrinterData**](/windows/desktop/printdocs/setprinterdata) définit les données de configuration d’une imprimante ou d’un serveur d’impression. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | La fonction [**SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex) définit les données de configuration d’une imprimante ou d’un serveur d’impression. La fonction stocke les données de configuration sous la clé de registre de l’imprimante. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | La fonction [**WritePrinter**](writeprinter.md) informe le spouleur d’impression que les données doivent être écrites sur l’imprimante spécifiée. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Fonctions de notification de modification d’imprimante

Ces fonctions permettent à une application d’être avertie des modifications apportées à l’état d’une imprimante.



| Fonction                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | La fonction [**FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) ferme un objet de notification de modification créé en appelant la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . L’imprimante ou le serveur d’impression associé à l’objet de notification de modification n’est plus analysé par cet objet. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | La fonction [**FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification) crée un objet de notification de modification et retourne un handle à l’objet. Vous pouvez ensuite utiliser ce handle dans un appel à l’une des fonctions Wait pour surveiller les modifications apportées à l’imprimante ou au serveur d’impression. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | La fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) récupère des informations sur la notification de modification la plus récente pour un objet de notification de modification associé à une imprimante ou à un serveur d’impression. Appelez cette fonction quand une opération d’attente sur l’objet de notification de modification est satisfaite. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | La fonction [**FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo) libère une mémoire tampon allouée par le système créée par la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Fonctions de formulaire d’imprimante

Ces fonctions gèrent les formulaires utilisés par une imprimante.



| Fonction                                    | Description                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | La fonction [**AddForm**](/windows/desktop/printdocs/addform) ajoute un formulaire à la liste des formulaires disponibles qui peuvent être sélectionnés pour l’imprimante spécifiée. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | La fonction [**DeleteForm**](/windows/desktop/printdocs/deleteform) supprime un nom de formulaire de la liste des formulaires pris en charge. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | La fonction [**EnumForms**](/windows/desktop/printdocs/enumforms) énumère les formulaires pris en charge par l’imprimante spécifiée. <br/>                               |
| [**GetForm**](getform.md)<br/>       | La fonction [**GetForm**](/windows/desktop/printdocs/getform) récupère des informations sur un formulaire spécifié. <br/>                                              |
| [**SetForm**](setform.md)<br/>       | La fonction [**SetForm**](/windows/desktop/printdocs/setform) définit les informations de formulaire pour l’imprimante spécifiée. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Fonctions du spouleur d’impression

Ces fonctions interagissent avec le spouleur d’impression à un niveau faible.



| Fonction                                                          | Description                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | La fonction [**CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle) ferme un handle vers un fichier de mise en file d’attente associé au travail d’impression actuellement soumis par l’application. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | La fonction [**CommitSpoolData**](/windows/desktop/printdocs/commitspooldata) informe le spouleur d’impression qu’une quantité de données spécifiée a été écrite dans un fichier spouleur spécifié et qu’elle est prête à être rendue. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | Le [**GetPrintExecutionData**](getprintexecutiondata.md) récupère le contexte d’impression actuel.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | La fonction [**GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle) récupère un handle pour le fichier de mise en file d’attente associé au travail actuellement soumis par l’application. <br/>                        |



 

 

