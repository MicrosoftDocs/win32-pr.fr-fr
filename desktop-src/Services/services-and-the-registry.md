---
description: Un service ne doit pas accéder à la \_ racine HKEY Current \_ User ou HKEY \_ classes \_ , en particulier lors de l’emprunt d’identité d’un utilisateur. Utilisez plutôt la fonction RegOpenCurrentUser ou RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Services et Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120769"
---
# <a name="services-and-the-registry"></a>Services et Registre

Un service ne doit pas accéder à la racine **HKEY \_ Current \_ User** ou **HKEY \_ classes \_**, en particulier lors de l’emprunt d’identité d’un utilisateur. Utilisez plutôt la fonction [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) ou [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .

Si vous tentez d’accéder à la racine **HKEY \_ Current \_ User** ou **HKEY \_ classes \_** à partir d’un service, cela peut échouer ou sembler fonctionner, mais il existe une fuite sous-jacente qui peut entraîner des problèmes lors du chargement ou du déchargement du profil utilisateur.

 

 
