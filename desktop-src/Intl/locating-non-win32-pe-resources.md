---
description: Recherche de ressources PE non Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Recherche de ressources PE non Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529134"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="486c8-103">Recherche de ressources PE non Win32</span><span class="sxs-lookup"><span data-stu-id="486c8-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="486c8-104">Pour localiser des ressources PE non Win32, votre application doit d’abord appeler la fonction [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) pour rechercher le fichier de ressources spécifique au langage à partir duquel charger les ressources.</span><span class="sxs-lookup"><span data-stu-id="486c8-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="486c8-105">Si l’application est conforme aux paramètres de langue système, elle doit appeler la fonction avec le \_ nom de langue MUI \_ langues de \| \_ \_ l’interface utilisateur par défaut de l’utilisateur MUI \_ \_ spécifié pour *dwFlags* et **null** spécifié pour *pwszLanguage*.</span><span class="sxs-lookup"><span data-stu-id="486c8-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="486c8-106">Si l’application suit les paramètres de langage spécifiques à l’application, elle utilise **GetFileMUIPath** pour déterminer si un fichier spécifique à la langue existe en spécifiant la langue dans le paramètre *pwszLanguage* .</span><span class="sxs-lookup"><span data-stu-id="486c8-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="486c8-107">Après l’appel à [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), l’application doit définir des fonctionnalités personnalisées pour charger le module de ressources et charger des ressources spécifiques à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="486c8-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="486c8-108">Par exemple, si vous utilisez un fichier de ressources. txt ou. xml, l’application doit utiliser un analyseur TXT ou XML pour charger le fichier, puis analyser le contenu du fichier pour chaque ressource requise.</span><span class="sxs-lookup"><span data-stu-id="486c8-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="486c8-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="486c8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="486c8-110">Utilisation de l’interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="486c8-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="486c8-111">**GetFileMUIPath**</span><span class="sxs-lookup"><span data-stu-id="486c8-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



