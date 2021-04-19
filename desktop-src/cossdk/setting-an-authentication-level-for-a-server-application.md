---
description: Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Définition d’un niveau d’authentification pour une application serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512897"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="39c3f-103">Définition d’un niveau d’authentification pour une application serveur</span><span class="sxs-lookup"><span data-stu-id="39c3f-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="39c3f-104">Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application.</span><span class="sxs-lookup"><span data-stu-id="39c3f-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="39c3f-105">Les niveaux d’authentification plus élevés fournissent une sécurité et une intégrité des données accrues, bien qu’ils entraînent généralement une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="39c3f-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="39c3f-106">Pour plus d’informations, consultez [authentification du client](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="39c3f-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="39c3f-107">**Pour sélectionner un niveau d’authentification pour une application serveur**</span><span class="sxs-lookup"><span data-stu-id="39c3f-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="39c3f-108">Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous configurez l’authentification, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="39c3f-109">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="39c3f-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="39c3f-110">Dans la zone **niveau d’authentification pour les appels** , sélectionnez le niveau approprié.</span><span class="sxs-lookup"><span data-stu-id="39c3f-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="39c3f-111">Les niveaux sont les suivants, triés de la sécurité la plus faible à la plus élevée :</span><span class="sxs-lookup"><span data-stu-id="39c3f-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="39c3f-112">**Aucun**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-112">**None**.</span></span> <span data-ttu-id="39c3f-113">Aucune authentification n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="39c3f-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="39c3f-114">**Connectez-vous**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-114">**Connect**.</span></span> <span data-ttu-id="39c3f-115">Authentifie les informations d'identification uniquement lorsque la connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="39c3f-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="39c3f-116">**Appelez**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-116">**Call**.</span></span> <span data-ttu-id="39c3f-117">Authentifie les informations d'identification au début de chaque appel.</span><span class="sxs-lookup"><span data-stu-id="39c3f-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="39c3f-118">**Paquet**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-118">**Packet**.</span></span> <span data-ttu-id="39c3f-119">Authentifie les informations d'identification et vérifie que toutes les données d'appel sont reçues.</span><span class="sxs-lookup"><span data-stu-id="39c3f-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="39c3f-120">Il s’agit du paramètre par défaut pour les applications serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="39c3f-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="39c3f-121">**Intégrité des paquets**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-121">**Packet Integrity**.</span></span> <span data-ttu-id="39c3f-122">Authentifie les informations d'identification et vérifie qu'aucune donnée d'appel n'a été modifiée lors du transit.</span><span class="sxs-lookup"><span data-stu-id="39c3f-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="39c3f-123">**Confidentialité du paquet**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-123">**Packet Privacy**.</span></span> <span data-ttu-id="39c3f-124">Authentifie les informations d'identification et chiffre le paquet, y compris les données et l'identité et la signature de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="39c3f-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="39c3f-125">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="39c3f-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39c3f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39c3f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39c3f-127">Activation de l’authentification pour une application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39c3f-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



