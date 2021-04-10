---
title: Gestionnaires de notifications d’administration
description: Le composant logiciel enfichable MMC utilisateurs et ordinateurs Microsoft Active Directory fournit un mécanisme pour permettre aux composants de recevoir des notifications lorsque l’utilisateur supprime, renomme, déplace ou modifie les propriétés d’un objet à l’aide du composant logiciel enfichable.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Gestionnaires de notifications d’administration Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa6f48f8b56ab8e4a1d64d0fe15543bfee6c09e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842102"
---
# <a name="administrative-notification-handlers"></a>Gestionnaires de notifications d’administration

Le composant logiciel enfichable MMC utilisateurs et ordinateurs Microsoft Active Directory fournit un mécanisme pour permettre aux composants de recevoir des notifications lorsque l’utilisateur supprime, renomme, déplace ou modifie les propriétés d’un objet à l’aide du composant logiciel enfichable. Le composant qui reçoit les notifications porte le nom de « gestionnaire de notifications ».

Cela est utile lorsque plusieurs objets sont liés et doivent exister dans le même conteneur. Si l’un des objets liés est déplacé, une notification est fournie au gestionnaire de notification et le gestionnaire de notification peut déplacer les autres objets liés dans le même dossier.

Lorsque l’une des opérations est effectuée et qu’un ou plusieurs gestionnaires de notification sont installés, le composant logiciel enfichable utilisateurs et ordinateurs affiche une boîte de dialogue de confirmation qui répertorie les gestionnaires de notification et une case à cocher pour chaque gestionnaire. Si la case à cocher d’un gestionnaire est activée, le gestionnaire est notifié. Si la case à cocher n’est pas activée, le gestionnaire n’est pas notifié.

## <a name="implementing-a-notification-handler"></a>Implémentation d’un gestionnaire de notification

Un gestionnaire de notifications est un objet COM implémenté en tant que serveur in-proc. Le gestionnaire de notifications doit implémenter l’interface [**IDsAdminNotifyHandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) .

Lorsqu’un événement qui génère une notification se produit, le composant logiciel enfichable utilisateurs et ordinateurs énumère les gestionnaires de notification enregistrés et crée chacun d’eux à l’aide du CLSID du gestionnaire. Une fois le gestionnaire créé, le composant logiciel enfichable appelle la méthode [**IDsAdminNotifyHandler :: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) . La méthode **Initialize** fournit au composant logiciel enfichable les événements que le gestionnaire doit recevoir.

Si l’événement est un événement qui doit être envoyé au gestionnaire de notifications, le composant logiciel enfichable appelle la méthode [**IDsAdminNotifyHandler :: Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) . La méthode **Begin** fournit le gestionnaire avec l’événement qui se produit, les données relatives à l’objet sur lequel l’événement se produit et, en fonction de l’événement, les données relatives à ce que l’objet va devenir. La méthode **Begin** fournit également le composant logiciel enfichable avec le texte qui doit être affiché pour le gestionnaire dans la boîte de dialogue de confirmation.

Lorsque la méthode [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) de chaque gestionnaire a été appelée, le composant logiciel enfichable affiche la boîte de dialogue de confirmation. La boîte de dialogue de confirmation invite l’utilisateur à sélectionner les gestionnaires qui recevront la notification. Si l’utilisateur appuie sur le bouton **aucun** push dans la boîte de dialogue de confirmation, aucun des gestionnaires n’est notifié. Si l’utilisateur appuie sur le bouton de commande **Oui** , chacun des gestionnaires sélectionnés dans la boîte de dialogue de confirmation reçoit la notification. Le composant logiciel enfichable envoie la notification au gestionnaire en appelant la méthode [**IDsAdminNotifyHandler :: Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) .

Une fois que tous les gestionnaires ont été notifiés, le composant logiciel enfichable appelle la méthode [**IDsAdminNotifyHandler :: end**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) . La méthode **end** est toujours appelée, même si la méthode [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) n’est pas appelée.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Inscription d’un gestionnaire de notifications dans le Registre Windows

Comme tous les serveurs COM, un gestionnaire de notifications doit être inscrit dans le Registre Windows. Le gestionnaire est inscrit sous la clé suivante :


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sous la **<CLSID>** clé, il existe une clé **InprocServer32** qui identifie l’objet en tant que serveur in-proc 32 bits. Sous la clé **InprocServer32** , l’emplacement de la dll est spécifié dans la valeur par défaut et le modèle de thread est spécifié dans la valeur **ThreadingModel** . Tous les gestionnaires de notification doivent utiliser le modèle de thread **cloisonné** .

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Inscription d’un gestionnaire de notifications auprès d’un serveur Active Directory

Dans Active Directory Domain Services, l’inscription du gestionnaire de notifications est spécifique à un paramètre régional. Si le gestionnaire de notifications s’applique à tous les paramètres régionaux, il doit être enregistré dans l’objet **displaySpecifier** dans tous les sous-conteneurs de paramètres régionaux du conteneur DisplaySpecifiers. Si le gestionnaire de notifications est localisé pour un certain nombre de paramètres régionaux, il est enregistré dans l’objet **displaySpecifier** dans le sous-conteneur de ces paramètres régionaux. Pour plus d’informations sur le conteneur DisplaySpecifiers et les paramètres régionaux, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).

Les gestionnaires de notification sont enregistrés sous l’attribut **dsUIAdminNotification** dans le conteneur **DS-UI-default-Settings** . Il s’agit d’une valeur de chaîne Unicode à valeurs multiples où chaque valeur requiert le format suivant :


```C++
<order number>,<CLSID>
```



« &lt; Order Number &gt; » est un nombre non signé qui représente la position du gestionnaire dans la boîte de dialogue de confirmation. Quand la boîte de dialogue de confirmation s’affiche, les valeurs sont triées à l’aide d’une comparaison de chaque valeur « &lt; Order Number &gt; ». Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces gestionnaires sont affichés dans l’ordre dans lequel ils sont lus à partir du serveur de Active Directory. Un non existant, autrement dit, qui n’est pas utilisé par d’autres valeurs de la propriété, « &lt; Order Number » (numéro de commande &gt; ) doit être utilisé si possible. Il n’y a pas de position de départ prescrite, et les intervalles peuvent apparaître dans la &lt; séquence « Order Number &gt; ».

Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID tel qu’il a été généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 