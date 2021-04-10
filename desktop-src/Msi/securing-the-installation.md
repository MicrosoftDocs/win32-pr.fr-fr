---
description: Ajoutez toutes les propriétés de mot de passe de la table CustomUserAccounts à la propriété MsiHiddenProperties dans la table des propriétés.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sécurisation de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953168"
---
# <a name="securing-the-installation"></a><span data-ttu-id="e1af6-103">Sécurisation de l’installation</span><span class="sxs-lookup"><span data-stu-id="e1af6-103">Securing the Installation</span></span>

<span data-ttu-id="e1af6-104">Ajoutez toutes les propriétés de mot de passe de la table CustomUserAccounts à la propriété [**MsiHiddenProperties**](msihiddenproperties.md) dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1af6-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="e1af6-105">Ajoutez également les noms des actions personnalisées différées à la propriété **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="e1af6-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="e1af6-106">Cela empêche le programme d’installation d’écrire les valeurs de propriété sensibles (les mots de passe) dans le journal et s’assure que ces valeurs ne sont pas journalisées lorsque les actions personnalisées différées utilisent les valeurs comme propriété CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="e1af6-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="e1af6-107">Pour que le mot de passe de l’utilisateur soit disponible dans le service Windows Installer, la propriété de mot de passe doit être ajoutée à la propriété [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e1af6-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="e1af6-108">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="e1af6-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="e1af6-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1af6-109">Property</span></span>                                                 | <span data-ttu-id="e1af6-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1af6-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e1af6-111">**MsiHiddenProperties**</span><span class="sxs-lookup"><span data-stu-id="e1af6-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="e1af6-112">TESTUSERPASSWORD; CreateAccount; RemoveAccount RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="e1af6-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="e1af6-113">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="e1af6-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="e1af6-114">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="e1af6-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="e1af6-115">Cela conclut l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e1af6-115">This concludes the sample.</span></span>

 

 



