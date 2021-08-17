---
title: Référence prise en charge pour les commandes PowerShell BITS
description: Service de transfert intelligent en arrière-plan (BITS) 4,0 peut utiliser des applets de commande Windows PowerShell pour gérer les tâches de transfert.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc88c557209ed2958d06766215278e75223a1b297bd2704ca1dcba062cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173855"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Référence prise en charge pour les commandes PowerShell BITS

Service de transfert intelligent en arrière-plan (BITS) 4,0 peut utiliser des applets de commande Windows PowerShell pour créer et gérer le téléchargement de fichiers et télécharger des tâches de transfert.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Windows PowerShell applets de commande pour BITS fournissent la plupart des fonctionnalités de l’utilitaire de ligne de commande bitsadmin. toutefois, Windows PowerShell effectue également les opérations suivantes :

-   Automatise les tâches BITS dans un langage de script extensible et orienté gestion.
-   Fournit un outil unique pour toutes les tâches liées au travail.

> [!Note]  
> Pour utiliser ces commandes, vous devez d’abord importer le module BITS PowerShell à l’aide de la `Import-Module BitsTransfer` commande. Pour plus d’informations, consultez l' [article TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10))suivant.

 

pour plus d’informations sur l’utilisation de Windows Powershell, consultez [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Classes PowerShell BITS

**Espace de noms**: Microsoft. BackgroundIntelligentTransfer. Management

**Assembly**: System. Management. Automation

Ces classes de commandes BITS sont implémentées par Windows PowerShell. Ces classes sont incluses dans ce kit de développement logiciel (SDK) à des fins d’exhaustivité uniquement. Les membres de ces classes ne peuvent pas être utilisés directement, ni être utilisés pour dériver d’autres classes.



| Classe                           | Description                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Ajoute un ou plusieurs fichiers à une tâche de transfert BITS existante.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) .<br/>                       |
| **ClearBitsTransferCommand**    | Annule une tâche de transfert BITS.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .<br/>                                          |
| **CompleteBitsTransferCommand** | Termine une tâche de transfert BITS.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .<br/>                                     |
| **GetBitsTransferCommand**      | Récupère l’objet BitsJob associé pour une tâche de transfert BITS existante.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/> |
| **NewBitsTransferCommand**      | Crée une tâche de transfert BITS.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                           |
| **ResumeBitsTransferCommand**   | Reprend une tâche de transfert BITS.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                            |
| **SetBitsTransferCommand**      | Modifie les propriétés d’une tâche de transfert BITS existante.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                  |
| **SuspendBitsTransferCommand**  | Interrompt une tâche de transfert BITS.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                          |



 

 

