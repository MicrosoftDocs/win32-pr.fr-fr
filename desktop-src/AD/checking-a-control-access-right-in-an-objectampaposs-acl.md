---
title: Vérification d’un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet
description: Pour vérifier un droit d’accès au contrôle dans la liste de contrôle d’accès d’un objet, utilisez la fonction AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Vérification d’un droit d’accès de contrôle dans une liste de contrôle d’accès d’objet Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031047"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="6a326-104">Vérification d’un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet</span><span class="sxs-lookup"><span data-stu-id="6a326-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="6a326-105">Pour vérifier un droit d’accès au contrôle dans la liste de contrôle d’accès d’un objet, utilisez la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .</span><span class="sxs-lookup"><span data-stu-id="6a326-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="6a326-106">Pour utiliser cette fonction, une application requiert un pointeur vers le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) de l’objet au lieu d’une interface [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) vers un objet com du descripteur de sécurité ADSI.</span><span class="sxs-lookup"><span data-stu-id="6a326-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="6a326-107">Procédez comme suit pour vérifier l’accès pour un droit d’accès contrôlé sur un objet :</span><span class="sxs-lookup"><span data-stu-id="6a326-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="6a326-108">Obtient un pointeur d’interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a326-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="6a326-109">Utilisez la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a326-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="6a326-110">Le nom de la propriété contenant le descripteur de sécurité est [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6a326-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="6a326-111">La propriété est retournée en tant que pointeur vers une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="6a326-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="6a326-112">Utilisez la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) avec la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) pour vérifier les autorisations pour le droit d’accès du contrôle spécifié pour le client spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a326-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="6a326-113">L’exemple de code dans l' [exemple de code pour la vérification d’un droit d’accès de contrôle dans l’ACL d’un objet](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) montre, en détail, comment procéder.</span><span class="sxs-lookup"><span data-stu-id="6a326-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 