---
description: Vous pouvez spécifier un descripteur de sécurité pour un canal anonyme quand vous appelez la fonction CreatePipe. Le descripteur de sécurité contrôle l’accès aux extrémités de lecture et d’écriture du canal.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sécurité des canaux anonymes et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528345"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="538ad-104">Sécurité des canaux anonymes et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="538ad-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="538ad-105">La sécurité Windows vous permet de contrôler l’accès aux canaux anonymes.</span><span class="sxs-lookup"><span data-stu-id="538ad-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="538ad-106">Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="538ad-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="538ad-107">Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un canal quand vous appelez la fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) .</span><span class="sxs-lookup"><span data-stu-id="538ad-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="538ad-108">Le descripteur de sécurité contrôle l’accès aux extrémités de lecture et d’écriture du canal.</span><span class="sxs-lookup"><span data-stu-id="538ad-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="538ad-109">Si vous spécifiez **null**, le canal obtient un descripteur de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="538ad-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="538ad-110">Les listes de contrôle d’accès dans le descripteur de sécurité par défaut pour un canal proviennent du jeton principal ou d’emprunt d’identité du créateur.</span><span class="sxs-lookup"><span data-stu-id="538ad-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="538ad-111">Pour récupérer le descripteur de sécurité d’un canal, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="538ad-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="538ad-112">Pour modifier le descripteur de sécurité d’un canal, appelez la fonction [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="538ad-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="538ad-113">La fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) retourne deux descripteurs au canal anonyme : un handle de lecture avec \_ accès de lecture et de synchronisation générique et un handle d’écriture avec un \_ accès d’écriture et de synchronisation générique.</span><span class="sxs-lookup"><span data-stu-id="538ad-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="538ad-114">\_L’accès en écriture générique en lecture et générique \_ utilisent le même mappage de droits d’accès que pour les canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="538ad-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="538ad-115">L' \_ accès en lecture générique pour un canal anonyme associe les droits de lecture des données du canal, de lecture des attributs de canal, de lecture des attributs étendus et de lecture de la liste DACL du canal.</span><span class="sxs-lookup"><span data-stu-id="538ad-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="538ad-116">L' \_ accès en écriture générique pour un canal anonyme combine les droits d’écriture de données sur le canal, y ajoute des données, écrit des attributs de canal, écrit des attributs étendus et lit la liste DACL du canal.</span><span class="sxs-lookup"><span data-stu-id="538ad-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
