---
description: La DLL de filtre de mot de passe Windows, Passfilt.dll, s’exécute dans le contexte de sécurité du compte système local et vous aide à filtrer les mots de passe de compte local ou de domaine.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installation et inscription d’une DLL de filtre de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865445"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="8c504-103">Installation et inscription d’une DLL de filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8c504-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="8c504-104">Vous pouvez utiliser le filtre de mot de passe Windows pour filtrer les mots de passe de compte local ou de domaine.</span><span class="sxs-lookup"><span data-stu-id="8c504-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="8c504-105">Pour utiliser le filtre de mot de passe pour les comptes de domaine, installez et inscrivez la DLL sur chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="8c504-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="8c504-106">Procédez comme suit pour installer votre filtre de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8c504-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="8c504-107">Vous pouvez effectuer ces étapes manuellement, ou vous pouvez écrire un programme d’installation pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="8c504-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="8c504-108">Pour effectuer ces étapes, vous devez être administrateur ou appartenir au groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8c504-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="8c504-109">**Pour installer et inscrire une DLL de filtre de mot de passe Windows**</span><span class="sxs-lookup"><span data-stu-id="8c504-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="8c504-110">Copiez la DLL dans le répertoire d’installation de Windows sur le contrôleur de domaine ou l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8c504-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="8c504-111">Sur les installations standard, le dossier par défaut est \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="8c504-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="8c504-112">Veillez à créer une DLL de filtre de mots de passe 32 bits pour les ordinateurs 32 bits et une DLL de filtre de mot de passe 64 bits pour les ordinateurs 64 bits, puis copiez-les à l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="8c504-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="8c504-113">Pour inscrire le filtre de mot de passe, mettez à jour la clé de Registre système suivante :</span><span class="sxs-lookup"><span data-stu-id="8c504-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="8c504-114">Si la sous-clé **packages de notification** existe, ajoutez le nom de votre dll aux données de la valeur existante.</span><span class="sxs-lookup"><span data-stu-id="8c504-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="8c504-115">Ne remplacez pas les valeurs existantes et n’incluez pas l’extension. dll.</span><span class="sxs-lookup"><span data-stu-id="8c504-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="8c504-116">Si la sous-clé **packages de notification** n’existe pas, ajoutez-la, puis spécifiez le nom de la dll pour les données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="8c504-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="8c504-117">N’incluez pas l’extension. dll.</span><span class="sxs-lookup"><span data-stu-id="8c504-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="8c504-118">La sous-clé **packages de notifications** peut ajouter plusieurs packages.</span><span class="sxs-lookup"><span data-stu-id="8c504-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="8c504-119">Recherchez le paramètre de complexité du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8c504-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="8c504-120">Dans le panneau de configuration, cliquez sur **performances et maintenance**, sur **Outils d’administration**, double-cliquez sur **stratégie de sécurité locale**, sur **stratégies de comptes**, puis sur **stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="8c504-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="8c504-121">Pour appliquer le filtre de mot de passe Windows par défaut et le filtre de mot de passe personnalisé, assurez-vous que le paramètre de stratégie les **mots de passe doivent respecter les exigences de complexité** est activé.</span><span class="sxs-lookup"><span data-stu-id="8c504-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="8c504-122">Dans le cas contraire, désactivez le paramètre de stratégie les **mots de passe doivent respecter des exigences de complexité** .</span><span class="sxs-lookup"><span data-stu-id="8c504-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c504-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c504-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c504-124">Considérations sur la programmation du filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8c504-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="8c504-125">Mise en œuvre des mots de passe forts et Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="8c504-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="8c504-126">Fonctions de filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8c504-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



