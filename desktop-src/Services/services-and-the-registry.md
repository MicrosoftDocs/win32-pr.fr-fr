---
description: Un service ne doit pas accéder à la \_ racine HKEY Current \_ User ou HKEY \_ classes \_ , en particulier lors de l’emprunt d’identité d’un utilisateur. Utilisez plutôt la fonction RegOpenCurrentUser ou RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Services et Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529208"
---
# <a name="services-and-the-registry"></a><span data-ttu-id="296b5-104">Services et Registre</span><span class="sxs-lookup"><span data-stu-id="296b5-104">Services and the Registry</span></span>

<span data-ttu-id="296b5-105">Un service ne doit pas accéder à la racine **HKEY \_ Current \_ User** ou **HKEY \_ classes \_**, en particulier lors de l’emprunt d’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296b5-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="296b5-106">Utilisez plutôt la fonction [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) ou [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .</span><span class="sxs-lookup"><span data-stu-id="296b5-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="296b5-107">Si vous tentez d’accéder à la racine **HKEY \_ Current \_ User** ou **HKEY \_ classes \_** à partir d’un service, cela peut échouer ou sembler fonctionner, mais il existe une fuite sous-jacente qui peut entraîner des problèmes lors du chargement ou du déchargement du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296b5-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
