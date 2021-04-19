---
description: 'Avant de placer des données dans le registre, une application doit diviser les données en deux catégories : données spécifiques à l’ordinateur et données spécifiques à l’utilisateur.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Catégories de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531429"
---
# <a name="categories-of-data"></a><span data-ttu-id="fb81f-103">Catégories de données</span><span class="sxs-lookup"><span data-stu-id="fb81f-103">Categories of Data</span></span>

<span data-ttu-id="fb81f-104">Avant de placer des données dans le registre, une application doit diviser les données en deux catégories : données spécifiques à l’ordinateur et données spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb81f-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="fb81f-105">En faisant cette distinction, une application peut prendre en charge plusieurs utilisateurs, tout en trouvant des données spécifiques à l’utilisateur sur un réseau et en utilisant ces données dans différents emplacements, ce qui permet d’obtenir des données de profil utilisateur indépendantes de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="fb81f-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="fb81f-106">(Un profil utilisateur est un ensemble de données de configuration enregistrées pour chaque utilisateur.)</span><span class="sxs-lookup"><span data-stu-id="fb81f-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="fb81f-107">Lorsque l’application est installée, elle doit enregistrer les données spécifiques à l’ordinateur sous la clé de l' **\_ \_ ordinateur local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fb81f-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="fb81f-108">En particulier, il doit créer des clés pour le nom de la société, le nom du produit et le numéro de version, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fb81f-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="fb81f-109">**HKEY \_ \_ \\ Logiciel \\ de l’ordinateur local**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="fb81f-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="fb81f-110">Si l’application prend en charge COM, elle doit enregistrer ces données sous **HKEY \_ local \_ machine \\ Software \\ classes**.</span><span class="sxs-lookup"><span data-stu-id="fb81f-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="fb81f-111">Une application doit enregistrer des données spécifiques à l’utilisateur sous la clé **HKEY \_ Current \_ User** , comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fb81f-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="fb81f-112">**HKEY \_ \_ \\ Logiciel \\ utilisateur actuel**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="fb81f-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



