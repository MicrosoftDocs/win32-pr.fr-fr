---
description: Dans certaines situations, les clés doivent être exportées à partir de l’environnement sécurisé du fournisseur de services de chiffrement (CSP) dans l’espace de données d’une application. Les clés qui ont été exportées sont stockées dans des structures BLOB de clé chiffrée.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Stockage de clé de chiffrement et Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515004"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="9ba65-104">Stockage de clé de chiffrement et Exchange</span><span class="sxs-lookup"><span data-stu-id="9ba65-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="9ba65-105">Dans certaines situations, les clés doivent être exportées à partir de l’environnement sécurisé du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) dans l’espace de données d’une application.</span><span class="sxs-lookup"><span data-stu-id="9ba65-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="9ba65-106">Les clés qui ont été exportées sont stockées dans des structures [*blob de clé*](../secgloss/k-gly.md) chiffrée.</span><span class="sxs-lookup"><span data-stu-id="9ba65-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="9ba65-107">Il existe deux situations spécifiques où il est nécessaire d’exporter des clés :</span><span class="sxs-lookup"><span data-stu-id="9ba65-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="9ba65-108">Pour enregistrer une [*clé de session*](../secgloss/s-gly.md) en vue d’une utilisation ultérieure par une application, si, par exemple, une application vient de chiffrer un fichier de base de données à déchiffrer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9ba65-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="9ba65-109">L’application est chargée de stocker la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9ba65-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="9ba65-110">Cela est nécessaire, car les fournisseurs de services de chiffrement ne préservent pas les [*clés symétriques*](../secgloss/s-gly.md) d’une session à l’autres.</span><span class="sxs-lookup"><span data-stu-id="9ba65-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="9ba65-111">Pour envoyer une clé à une autre personne.</span><span class="sxs-lookup"><span data-stu-id="9ba65-111">To send a key to someone else.</span></span> <span data-ttu-id="9ba65-112">Cela serait plus facile si les fournisseurs de services de chiffrement respectifs pouvaient communiquer directement, mais ils ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="9ba65-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="9ba65-113">Étant donné que les fournisseurs de services de chiffrement ne peuvent pas communiquer, la clé doit être exportée à partir d’un CSP, transmise à l’application de destination, puis importée dans le CSP de destination.</span><span class="sxs-lookup"><span data-stu-id="9ba65-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="9ba65-114">Ce processus peut devenir plus compliqué si le chemin de communication n’est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="9ba65-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="9ba65-115">Dans les deux cas, une application doit stocker une clé de session en dehors du CSP pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="9ba65-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="9ba65-116">Pour plus d’informations, consultez [procédure de stockage d’une clé de session](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="9ba65-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
