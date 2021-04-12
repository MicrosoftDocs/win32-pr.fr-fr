---
description: Les certificats sont accordés conformément aux stratégies qui définissent les critères que les demandeurs doivent remplir pour recevoir un certificat.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Indépendance de la stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319590"
---
# <a name="policy-independence"></a><span data-ttu-id="cfec0-103">Indépendance de la stratégie</span><span class="sxs-lookup"><span data-stu-id="cfec0-103">Policy Independence</span></span>

<span data-ttu-id="cfec0-104">Les certificats sont accordés conformément aux stratégies qui définissent les critères que les demandeurs doivent remplir pour recevoir un certificat.</span><span class="sxs-lookup"><span data-stu-id="cfec0-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="cfec0-105">Par exemple, une stratégie peut être d’accorder des certificats commerciaux uniquement si les candidats présentent leur identification en personne.</span><span class="sxs-lookup"><span data-stu-id="cfec0-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="cfec0-106">Une autre stratégie peut accorder des [*informations d’identification*](../secgloss/c-gly.md) en fonction des demandes par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="cfec0-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="cfec0-107">Une agence qui émet des cartes de crédit peut choisir de consulter une base de données et de faire des demandes de téléphone avant d’émettre une carte.</span><span class="sxs-lookup"><span data-stu-id="cfec0-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="cfec0-108">Les stratégies sont implémentées dans des modules de stratégie écrits en C++, C ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cfec0-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="cfec0-109">Les fonctions des services de certificats sont isolées des modifications apportées à la stratégie qu’une Agence peut implémenter.</span><span class="sxs-lookup"><span data-stu-id="cfec0-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="cfec0-110">Les modifications apportées à la stratégie peuvent être entièrement implémentées dans le code du module de stratégie serveur.</span><span class="sxs-lookup"><span data-stu-id="cfec0-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="cfec0-111">Une [*autorité de certification*](../secgloss/c-gly.md) d’entreprise (ca) doit utiliser uniquement le module de stratégie d’entreprise fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfec0-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
