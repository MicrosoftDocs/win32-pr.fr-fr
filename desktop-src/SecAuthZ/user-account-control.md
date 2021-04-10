---
description: Permet aux utilisateurs d’effectuer des tâches courantes en tant que non-administrateurs, appelées utilisateurs standard et en tant qu’administrateurs sans avoir à changer d’utilisateur, à fermer la session ou à utiliser exécuter en tant que.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Contrôle de compte d’utilisateur (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952718"
---
# <a name="user-account-control-authorization"></a>Contrôle de compte d’utilisateur (autorisation)

Le contrôle de compte d’utilisateur (UAC) permet aux utilisateurs d’effectuer des tâches courantes en tant que non-administrateurs, appelées utilisateurs standard et en tant qu’administrateurs sans avoir à changer d’utilisateur, à fermer la session ou à utiliser **exécuter en tant que**. Le comportement du contrôle de compte d’utilisateur pour le paramètre « ne jamais notifier » ne désactive plus le contrôle de compte d’utilisateur. Le paramètre « ne jamais notifier » vous donne un jeton de fractionnement et élève toujours automatiquement le privilège requis. Cette subtilité peut entraîner des problèmes de compatibilité avec votre application. Vous pouvez toujours désactiver le contrôle de compte d’utilisateur en utilisant des stratégies de groupe ou en définissant manuellement la clé de registre.

**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Le paramètre « ne jamais notifier » désactive le contrôle de compte d’utilisateur.

Par exemple, si vous effectuez les étapes suivantes pour modifier le paramètre « ne jamais notifier », vous pouvez obtenir des résultats différents lorsque vous essayez de créer un fichier dans un dossier qui nécessite des privilèges élevés. Le comportement de Windows 8 est de refuser l’accès. Le comportement de Windows 7 vous permet de créer le fichier File.txt.

1.  Cliquez ou appuyez sur **Start**. Dans la zone de recherche, tapez « modifier les paramètres de contrôle de compte d’utilisateur ».
2.  Cliquez ou appuyez sur **modifier les paramètres du contrôle de compte d’utilisateur** pour l’ouvrir.
3.  Déplacez le curseur sur **ne jamais notifier**.
4.  Cliquez ou appuyez sur **OK**.
5.  Redémarrez votre ordinateur.
6.  Cliquez ou appuyez sur **Démarrer** , puis sur **exécuter**. Dans la zone **ouvrir** , tapez « Cmd.exe ». Notez que le titre de la fenêtre ne contient pas la chaîne « administrateur ».
7.  Tapez « Echo >% windir% \\ system32 \\File.txt ».

Le contrôle de compte d’utilisateur a été ajouté dans Windows Server 2008 et Windows Vista. Un compte d’utilisateur standard est synonyme d’un compte d’utilisateur dans Windows XP. Les comptes d’utilisateurs qui sont membres du groupe Administrateurs local exécutent la plupart des applications en tant qu’utilisateur standard.

Pour plus d’informations sur le contrôle de compte d’utilisateur, consultez les rubriques suivantes.



| Rubrique                                                                                                                                        | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Instructions pour le contrôle de compte d’utilisateur dans le développement d’interface utilisateur](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Informations générales sur le contrôle de compte d’utilisateur.<br/>                                                                                                     |
| [Développement d’applications nécessitant des privilèges d’administrateur](developing-applications-that-require-administrator-privilege.md)<br/>  | Modèles pour le développement d’applications qui effectuent des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécutent en tant qu’utilisateur standard.<br/> |
| [Référence d’autorisation](authorization-reference.md)<br/>                                                                            | Informations détaillées sur les fonctions d’autorisation, les interfaces, les structures et d’autres éléments de programmation.<br/>                        |



 

 

 




