---
description: L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Utilisation de SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114122"
---
# <a name="using-setreg"></a><span data-ttu-id="fef47-103">Utilisation de SetReg</span><span class="sxs-lookup"><span data-stu-id="fef47-103">Using SetReg</span></span>

<span data-ttu-id="fef47-104">L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode.</span><span class="sxs-lookup"><span data-stu-id="fef47-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="fef47-105">Ces clés, appelées clés d’état de publication de logiciels, déterminent s’il faut approuver une racine de test, autoriser l’approbation hors connexion des certificats, tester les dates d’expiration des certificats et effectuer des vérifications de révocation.</span><span class="sxs-lookup"><span data-stu-id="fef47-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="fef47-106">La commande suivante répertorie la syntaxe et les options d’utilisation de SetReg.</span><span class="sxs-lookup"><span data-stu-id="fef47-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="fef47-107">**setreg- ?**</span><span class="sxs-lookup"><span data-stu-id="fef47-107">**setreg -?**</span></span>

<span data-ttu-id="fef47-108">La commande suivante rend une racine de test approuvée.</span><span class="sxs-lookup"><span data-stu-id="fef47-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="fef47-109">Par défaut, une racine de test n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="fef47-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="fef47-110">Une fois les modifications apportées aux valeurs de clé effectuées, une liste de la valeur actuelle de toutes les valeurs de clé s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fef47-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="fef47-111">Si l’option **-q** est utilisée, les valeurs de clé ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="fef47-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="fef47-112">**setreg 1 TRUE**</span><span class="sxs-lookup"><span data-stu-id="fef47-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="fef47-113">La commande suivante rend une racine de test non fiable et entraîne la vérification de la révocation de toutes les vérifications.</span><span class="sxs-lookup"><span data-stu-id="fef47-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="fef47-114">L’option **-q** est utilisée pour que la liste des valeurs de clés ne s’affiche pas</span><span class="sxs-lookup"><span data-stu-id="fef47-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="fef47-115">**setreg-q 1 faux 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="fef47-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="fef47-116">Les commandes, les options et les arguments ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="fef47-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



