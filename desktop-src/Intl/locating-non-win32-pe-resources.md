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
# <a name="locating-non-win32-pe-resources"></a>Recherche de ressources PE non Win32

Pour localiser des ressources PE non Win32, votre application doit d’abord appeler la fonction [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) pour rechercher le fichier de ressources spécifique au langage à partir duquel charger les ressources. Si l’application est conforme aux paramètres de langue système, elle doit appeler la fonction avec le \_ nom de langue MUI \_ langues de \| \_ \_ l’interface utilisateur par défaut de l’utilisateur MUI \_ \_ spécifié pour *dwFlags* et **null** spécifié pour *pwszLanguage*. Si l’application suit les paramètres de langage spécifiques à l’application, elle utilise **GetFileMUIPath** pour déterminer si un fichier spécifique à la langue existe en spécifiant la langue dans le paramètre *pwszLanguage* .

Après l’appel à [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), l’application doit définir des fonctionnalités personnalisées pour charger le module de ressources et charger des ressources spécifiques à partir de celui-ci. Par exemple, si vous utilisez un fichier de ressources. txt ou. xml, l’application doit utiliser un analyseur TXT ou XML pour charger le fichier, puis analyser le contenu du fichier pour chaque ressource requise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’interface utilisateur multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



