---
description: Vous pouvez contrôler la capacité d’un processus à accéder aux objets sécurisables ou à effectuer des tâches d’administration système.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Spécification d’un descripteur de sécurité à partir d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952996"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="d7ac6-103">Spécification d’un descripteur de sécurité à partir d’un fichier INF</span><span class="sxs-lookup"><span data-stu-id="d7ac6-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="d7ac6-104">Vous pouvez contrôler la capacité d’un processus à accéder aux objets sécurisables ou à effectuer des tâches d’administration système.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="d7ac6-105">Un objet sécurisable est un objet qui peut avoir un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="d7ac6-106">Tous les objets nommés sont sécurisables.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-106">All named objects are securable.</span></span> <span data-ttu-id="d7ac6-107">Certains objets sans nom, tels que les objets de processus et de thread, peuvent également avoir des descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="d7ac6-108">Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="d7ac6-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="d7ac6-109">Les [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors) contiennent les informations de sécurité associées aux objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="d7ac6-110">Pour la plupart des objets sécurisables, vous pouvez spécifier le descripteur de sécurité d’un objet dans l’appel de fonction qui crée l’objet.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="d7ac6-111">Par exemple, vous pouvez spécifier un descripteur de sécurité dans les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="d7ac6-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="d7ac6-112">Pour définir un descripteur de sécurité à partir d’un fichier INF, ajoutez une section sécurité créée par l’enregistreur INF immédiatement après la section qui installe le fichier, la clé de registre ou le composant.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="d7ac6-113">La section sécurité doit contenir une ligne avec le descripteur de sécurité de chaîne écrit en utilisant le format pour les [chaînes de descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-strings).</span><span class="sxs-lookup"><span data-stu-id="d7ac6-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="d7ac6-114">La ligne doit également être placée entre guillemets (").</span><span class="sxs-lookup"><span data-stu-id="d7ac6-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="d7ac6-115">Par exemple, l’extrait de code fichier INF suivant crée une clé de Registre à laquelle seuls les administrateurs et le système ont accès.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="d7ac6-116">Notez que cet exemple requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="d7ac6-117">Dans ce cas, la signification de la chaîne est que les administrateurs disposent d’un contrôle total, que le système dispose d’un contrôle total et que l’accès peut être hérité à toutes les sous-clés.</span><span class="sxs-lookup"><span data-stu-id="d7ac6-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="d7ac6-118">Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="d7ac6-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
