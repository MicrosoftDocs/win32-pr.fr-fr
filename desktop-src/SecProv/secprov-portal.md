---
description: Les fournisseurs WMI de sécurité peuvent être utilisés pour les scripts WMI et pour créer un fournisseur de sécurité managé.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Fournisseurs WMI de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581987"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="ca02f-103">Fournisseurs WMI de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca02f-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="ca02f-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="ca02f-104">Purpose</span></span>

<span data-ttu-id="ca02f-105">les fournisseurs wmi de sécurité permettent aux administrateurs et aux programmeurs de configurer Chiffrement de lecteur BitLocker (BDE) et le Module de plateforme sécurisée (TPM) (TPM) à l’aide d’Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ca02f-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ca02f-106">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="ca02f-106">Developer audience</span></span>

<span data-ttu-id="ca02f-107">ce document spécifie l’interface du fournisseur WMI pour la gestion et la configuration de Chiffrement de lecteur BitLocker (BDE) et Module de plateforme sécurisée (TPM) (TPM) sur Windows server 2008 R2 et Windows server 2008 pour les serveurs, ainsi que Windows 7 et Windows Vista pour les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="ca02f-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="ca02f-108">Elle est destinée à être lue par les scripts d’écriture, les éléments de l’interface utilisateur ou d’autres outils d’administration pour BDE ou le TPM.</span><span class="sxs-lookup"><span data-stu-id="ca02f-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ca02f-109">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="ca02f-109">Run-time requirements</span></span>

<span data-ttu-id="ca02f-110">Les fournisseurs WMI de sécurité requièrent le fichier. mof spécifié avec chaque fournisseur et un système d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ca02f-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="ca02f-111">le système d’exploitation minimal est Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca02f-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca02f-112">Chiffrement de lecteur BitLocker est disponible uniquement pour les versions Windows vista Enterprise et Windows vista Ultimate de Windows vista.</span><span class="sxs-lookup"><span data-stu-id="ca02f-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="ca02f-113">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ca02f-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca02f-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ca02f-114">In this section</span></span>



| <span data-ttu-id="ca02f-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ca02f-115">Topic</span></span>                                                                               | <span data-ttu-id="ca02f-116">Description</span><span class="sxs-lookup"><span data-stu-id="ca02f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ca02f-117">À propos des fournisseurs WMI de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca02f-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="ca02f-118">Bref aperçu des fournisseurs WMI de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ca02f-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="ca02f-119">Informations de référence sur les fournisseurs WMI de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca02f-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="ca02f-120">Documentation de référence pour les fournisseurs WMI de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ca02f-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="ca02f-121">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ca02f-121">Additional resources</span></span>

<span data-ttu-id="ca02f-122">Vous trouverez ci-dessous des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ca02f-122">The following are additional resources.</span></span>



| <span data-ttu-id="ca02f-123">Ressource</span><span class="sxs-lookup"><span data-stu-id="ca02f-123">Resource</span></span>     | <span data-ttu-id="ca02f-124">Description</span><span class="sxs-lookup"><span data-stu-id="ca02f-124">Description</span></span>                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca02f-125">Classes</span><span class="sxs-lookup"><span data-stu-id="ca02f-125">Classes</span></span>      | <span data-ttu-id="ca02f-126">Pour plus d’informations sur les fournisseurs WMI de sécurité, consultez [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) et [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="ca02f-126">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span> |



 

 

 




