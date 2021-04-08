---
title: Annuaires RAS
description: Les annuaires téléphoniques offrent un moyen standard de collecter et de spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir une connexion à distance.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Annuaires téléphoniques, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029309"
---
# <a name="ras-phone-books"></a><span data-ttu-id="7428e-104">Annuaires RAS</span><span class="sxs-lookup"><span data-stu-id="7428e-104">RAS Phone Books</span></span>

<span data-ttu-id="7428e-105">Les annuaires téléphoniques offrent un moyen standard de collecter et de spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="7428e-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="7428e-106">Les livres téléphoniques associent des noms d’entrée à des informations telles que des numéros de téléphone, des ports COM et des paramètres de modem.</span><span class="sxs-lookup"><span data-stu-id="7428e-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="7428e-107">Chaque entrée de l’annuaire téléphonique contient les informations nécessaires pour établir une connexion RAS.</span><span class="sxs-lookup"><span data-stu-id="7428e-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="7428e-108">Les annuaires téléphoniques sont stockés dans des fichiers de l’annuaire, qui sont des fichiers texte qui contiennent les noms d’entrée et les informations associées.</span><span class="sxs-lookup"><span data-stu-id="7428e-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="7428e-109">RAS crée un fichier d’annuaire téléphonique nommé RASPHONE. PBK.</span><span class="sxs-lookup"><span data-stu-id="7428e-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="7428e-110">L’utilisateur peut utiliser la boîte de dialogue principale d' **accès réseau à distance** pour créer des fichiers de l’annuaire téléphonique personnel.</span><span class="sxs-lookup"><span data-stu-id="7428e-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="7428e-111">L’API RAS ne prend pas actuellement en charge la création d’un fichier d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="7428e-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="7428e-112">Certaines fonctions RAS, telles que la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , ont un paramètre qui spécifie un fichier d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="7428e-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="7428e-113">Si l’appelant ne spécifie pas de fichier d’annuaire téléphonique, la fonction utilise le fichier de l’annuaire téléphonique par défaut, qui est celui sélectionné par l’utilisateur dans la feuille de propriétés préférences de l' **utilisateur** de la boîte de dialogue **accès réseau à distance** .</span><span class="sxs-lookup"><span data-stu-id="7428e-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="7428e-114">Windows NT 4,0 fournit les fonctions [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) et [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) qui affichent l’interface utilisateur RAS intégrée qui permet aux utilisateurs d’utiliser des annuaires téléphoniques et des entrées d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="7428e-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="7428e-115">**Windows 95 :** L’accès réseau à distance stocke les entrées d’annuaire téléphonique dans le registre plutôt que dans un fichier d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="7428e-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="7428e-116">Windows 95 ne prend pas en charge les fichiers de l’annuaire téléphonique personnel ou les fonctions qui affichent les boîtes de dialogue intégrées RAS.</span><span class="sxs-lookup"><span data-stu-id="7428e-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




