---
description: L’interface TAPI assigne des identificateurs de session qui sont uniques pour chaque session et application.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificateur de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393803"
---
# <a name="session-identifier"></a><span data-ttu-id="051e2-103">Identificateur de session</span><span class="sxs-lookup"><span data-stu-id="051e2-103">Session Identifier</span></span>

<span data-ttu-id="051e2-104">L’interface TAPI assigne des identificateurs de session qui sont uniques pour chaque session et application.</span><span class="sxs-lookup"><span data-stu-id="051e2-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="051e2-105">Une application utilise un identificateur de session pour communiquer avec l’interface TAPI concernant une session spécifique.</span><span class="sxs-lookup"><span data-stu-id="051e2-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="051e2-106">Une application obtient généralement un identificateur en créant une session de communication ou lorsque l’interface TAPI offre une session.</span><span class="sxs-lookup"><span data-stu-id="051e2-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="051e2-107">Un identificateur de session ne peut pas être utilisé pour transmettre des informations à une autre application.</span><span class="sxs-lookup"><span data-stu-id="051e2-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="051e2-108">À cet effet, utilisez l' [ID d’appel](call-id-ovr.md), qui peut être assigné par un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="051e2-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="051e2-109">Consultez [lancer une session](initiate-a-session-ovr.md) pour plus d’informations sur les opérations qui créent des sessions et retournent un identificateur de session.</span><span class="sxs-lookup"><span data-stu-id="051e2-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="051e2-110">Consultez [répondre à la session lancée ailleurs](respond-to-session-initiated-elsewhere-ovr.md) pour les opérations qui acquièrent des identificateurs de session à partir de TAPI.</span><span class="sxs-lookup"><span data-stu-id="051e2-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="051e2-111">Pour plus d’informations sur la libération des ressources de session, consultez [terminer une session](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="051e2-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="051e2-112">Tous les fournisseurs de services doivent prendre en charge une certaine forme d’identification de session.</span><span class="sxs-lookup"><span data-stu-id="051e2-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="051e2-113">**TAPI 2. x :** L’identificateur principal d’une session de communication est le descripteur d’appel.</span><span class="sxs-lookup"><span data-stu-id="051e2-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="051e2-114">**TAPI 3. x :** Une session est représentée par un [objet d’appel](call-object.md) et l’identificateur principal est un pointeur vers l’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="051e2-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



