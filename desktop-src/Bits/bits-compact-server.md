---
title: BITS Compact Server
description: Le serveur compact Server Service de transfert intelligent en arrière-plan (BITS) est un serveur de fichiers HTTP/HTTPs autonome qui permet de transférer de façon asynchrone un nombre limité de fichiers volumineux entre les ordinateurs.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842525"
---
# <a name="bits-compact-server"></a>BITS Compact Server

Le serveur compact Server Service de transfert intelligent en arrière-plan (BITS) est un serveur de fichiers HTTP/HTTPs autonome qui permet de transférer de façon asynchrone un nombre limité de fichiers volumineux entre les ordinateurs. Le serveur compact est construit en tant que service NT et utilise HTTP.SYS.

Le serveur BITS Compact Server est destiné aux entreprises et aux petites entreprises dans les conditions suivantes :

-   L’utilisation anticipée est un maximum de 25 groupes d’URL, et chaque groupe d’URL prend en charge 3 transferts de fichiers simultanés.
-   Les transferts de fichiers se produisent entre des ordinateurs dans le même domaine ou des domaines approuvés mutuellement.
-   Les transferts de fichiers ne sont pas destinés aux clients accessibles sur Internet.

## <a name="installing-the-bits-compact-server"></a>Installation de BITS Compact Server

BITS Compact Server est un composant serveur facultatif. Vous pouvez utiliser l’une des options suivantes pour installer BITS Compact Server :

-   Gestionnaire de serveur

-   Windows PowerShell

-   Gestionnaire de package

**Pour installer BITS Compact Server à l’aide de Gestionnaire de serveur**

1.  Dans la section **Résumé des fonctionnalités** de la **Gestionnaire de serveur**, cliquez sur Ajouter des **fonctionnalités**.
2.  Dans l’Assistant Ajout de fonctionnalités, sélectionnez **service de transfert intelligent en arrière-plan (bits)** et **Compact Server**.
3.  Suivez les instructions de l’Assistant, y compris l’installation des logiciels requis, le cas échéant.

Pour plus d’informations, consultez l’aide en ligne de **Gestionnaire de serveur** .

**Pour installer BITS Compact Server à l’aide de Windows PowerShell**

1.  Dans une invite de commandes Windows PowerShell, tapez la commande suivante : **import-module ServerManager**. Appuyez sur Entrée.
2.  Tapez la commande suivante : **Add-WINDOWSFEATURE bits-Compact-Server**. Appuyez sur Entrée.

L’exemple de texte suivant illustre l’installation de BITS Compact Server à l’aide des applets de commande Windows PowerShell.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Pour plus d’informations sur l’utilisation des applets de commande, consultez la documentation de [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

Pour plus d’informations sur l’applet de commande Import-Module, consultez [import-module](/previous-versions//dd347701(v=technet.10)) dans la bibliothèque Microsoft TechNet. Pour obtenir de l’aide à partir de la ligne de commande, tapez **« obtenir-aide import-module »**.

Pour plus d’informations sur l’applet de commande Add-WindowsFeature, consultez [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) dans la bibliothèque Microsoft TechNet. Pour obtenir de l’aide sur la ligne de commande, tapez **« obtenir-help Add-WindowsFeature »**.

**Pour installer BITS Compact Server à l’aide du gestionnaire de package**

-   Entrez la commande suivante : **PkgMgr.exe/IU : LightweightServer**.

> [!Note]  
> Les paramètres sont perdus si le service Compact Server est redémarré ou si l’ordinateur est redémarré.

 

## <a name="bits-compact-server-remote-management"></a>Gestion à distance de BITS Compact Server

Le serveur BITS Compact avec la gestion à distance BITS permet des transferts de fichiers à distance plus sécurisés. La gestion à distance BITS utilise un fournisseur de Windows Management Instrumentation (WMI) pour permettre à un administrateur système ou à une application de contrôleur de créer à distance des tâches de transfert BITS sur les clients et de publier des fichiers pour l’hébergement sur le serveur BITS Compact Server. Le fournisseur BITS peut également être utilisé pour permettre à une application d’utiliser à distance le client BITS conjointement avec le serveur BITS Compact Server pour transférer des fichiers d’un ordinateur distant à un autre ordinateur distant.

Pour plus d’informations, consultez la documentation du [fournisseur bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseur BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 