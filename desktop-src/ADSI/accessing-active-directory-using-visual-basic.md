---
title: Accès Active Directory à l’aide de Visual Basic
description: L’une des fonctionnalités les plus puissantes qui sont devenues disponibles avec le système d’exploitation Microsoft Windows 2000 est le service d’annuaire Microsoft Active Directory.
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- Accès Active Directory à l’aide de l’interface ADSI Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028579"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="c1c38-104">Accès Active Directory à l’aide de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c1c38-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="c1c38-105">L’une des fonctionnalités les plus puissantes qui sont devenues disponibles avec le système d’exploitation Microsoft Windows 2000 est le service d’annuaire Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1c38-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="c1c38-106">Quand vous vous connectez à un domaine Windows 2000, Active Directory est mis en action ; pour Rechercher l’imprimante couleur la plus proche dans votre bâtiment, vous pouvez utiliser Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1c38-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="c1c38-107">Il peut être utilisé pour une recherche de carnet d’adresses ou une recherche pour les utilisateurs qui travaillent dans le bâtiment 40.</span><span class="sxs-lookup"><span data-stu-id="c1c38-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="c1c38-108">Avec Active Directory, vous pouvez utiliser une carte à puce pour ouvrir une session sur un domaine Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c1c38-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="c1c38-109">Vous pouvez même joindre des données à partir de Microsoft SQL Server logiciel et Active Directory de base de données.</span><span class="sxs-lookup"><span data-stu-id="c1c38-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="c1c38-110">De nombreuses autres technologies Microsoft, telles que Microsoft Message Queue Server (MSMQ), COM (Store de classes), IPsec (Internet Protocol Security), les objets de stratégie de groupe (GPO) et Exchange sont intégrées à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1c38-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="c1c38-111">Cette section explique comment utiliser les interfaces de service Active Directory (ADSI) pour accéder à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1c38-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="c1c38-112">À l’aide d’un scénario pour une société fictive (Fabrikam Corporation), vous apprendrez à effectuer certaines tâches d’administration de base.</span><span class="sxs-lookup"><span data-stu-id="c1c38-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="c1c38-113">Au fur et à mesure que vous progressez dans ce scénario, les exemples de code de chaque section s’appuient sur eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="c1c38-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="c1c38-114">Par souci de concision, tous les exemples de code sont écrits avec le système de développement Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1c38-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="c1c38-115">Pour plus d’informations sur la conversion C++, consultez [mappage d’ADSI Visual Basic du code au code C++](mapping-adsi-visual-basic-code-to-c-code.md).</span><span class="sxs-lookup"><span data-stu-id="c1c38-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




