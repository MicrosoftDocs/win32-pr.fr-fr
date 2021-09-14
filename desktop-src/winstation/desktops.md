---
title: Bureaux
description: Un bureau a une surface d’affichage logique et contient des objets d’interface utilisateur tels que des fenêtres, des menus et des raccordements. Il peut être utilisé pour créer et gérer des fenêtres.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- objets de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ca0b390ec4d34cc943c9d18d958cdea6466634
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404486"
---
# <a name="desktops"></a>Bureaux

Un *Bureau* a une surface d’affichage logique et contient des objets d’interface utilisateur tels que des fenêtres, des menus et des raccordements. Il peut être utilisé pour créer et gérer des fenêtres. Chaque objet Desktop est un objet sécurisable. Lorsqu’un bureau est créé, il est associé à la [station de fenêtre](window-stations.md) active du processus appelant et affecté au thread appelant.

Les messages de fenêtre peuvent être envoyés uniquement entre des processus qui se trouvent sur le même bureau. En outre, la procédure de raccordement d’un processus exécuté sur un poste de travail particulier peut uniquement recevoir des messages destinés aux fenêtres créées dans le même bureau.

Les postes de travail associés à la station Windows Interactive, Winsta0, peuvent être créés pour afficher une interface utilisateur et recevoir l’entrée utilisateur, mais un seul de ces bureaux à la fois est actif. Ce bureau actif, également connu sous le nom de *Bureau d’entrée*, est celui qui est actuellement visible par l’utilisateur et qui reçoit les entrées d’utilisateur. Les applications peuvent utiliser la fonction [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) pour obtenir un handle vers le Bureau d’entrée. Les applications qui disposent de l’accès requis peuvent utiliser la fonction [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) pour spécifier un autre bureau d’entrée.

Par défaut, il existe trois bureaux dans la station Windows Interactive : par défaut, économiseurs d’écran et Winlogon.

Le bureau par défaut est créé lorsque Winlogon démarre le processus initial en tant qu’utilisateur connecté. À ce stade, le bureau par défaut devient actif et il est utilisé pour interagir avec l’utilisateur.

Chaque fois qu’un économiseur d’écran sécurisé est activé, le système bascule automatiquement vers le Bureau de l’écran de veille, qui protège les processus sur le bureau par défaut des utilisateurs non autorisés. Les économiseurs d’écran non sécurisés s’exécutent sur Winsta0 \\ par défaut.

Le bureau Winlogon est actif lorsqu’un utilisateur ouvre une session. Le système bascule sur le bureau par défaut lorsque l’interpréteur de commandes indique qu’il est prêt à afficher un événement, ou après trente secondes, le cas échéant. Pendant la session de l’utilisateur, le système bascule vers le Bureau de Winlogon quand l’utilisateur appuie sur la séquence de touches CTRL + ALT + SUPPR, ou lorsque la boîte de dialogue contrôle de compte d’utilisateur (UAC) est ouverte.

**Windows Server 2003 et Windows XP/2000 :** La boîte de dialogue contrôle de compte d’utilisateur n’est pas prise en charge.

Le descripteur de sécurité de Winlogon Desktop autorise l’accès à un ensemble de comptes très restreint, y compris le [compte LocalSystem](/windows/desktop/Services/localsystem-account). En règle générale, les applications ne transmettent pas les SID de ces comptes dans leurs jetons et ne peuvent donc pas accéder au bureau Winlogon ni basculer vers un autre bureau lorsque le bureau Winlogon est actif.

Pour plus d'informations, voir les rubriques suivantes :

-   [Station Windows et création de bureau](window-station-and-desktop-creation.md)
-   [Connexion de thread à un bureau](thread-connection-to-a-desktop.md)
-   [Sécurité des postes de travail et droits d’accès](desktop-security-and-access-rights.md)

 

 