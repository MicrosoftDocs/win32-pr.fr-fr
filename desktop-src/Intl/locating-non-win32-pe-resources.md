---
description: Recherche de ressources PE non Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Recherche de ressources PE non Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147172"
---
# <a name="locating-non-win32-pe-resources"></a>Recherche de ressources PE non Win32

Pour localiser des ressources PE non Win32, votre application doit d’abord appeler la fonction [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) pour rechercher le fichier de ressources spécifique au langage à partir duquel charger les ressources. Si l’application est conforme aux paramètres de langue système, elle doit appeler la fonction avec le \_ nom de langue MUI \_ langues de \| \_ \_ l’interface utilisateur par défaut de l’utilisateur MUI \_ \_ spécifié pour *dwFlags* et **null** spécifié pour *pwszLanguage*. Si l’application suit les paramètres de langage spécifiques à l’application, elle utilise **GetFileMUIPath** pour déterminer si un fichier spécifique à la langue existe en spécifiant la langue dans le paramètre *pwszLanguage* .

Après l’appel à [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), l’application doit définir des fonctionnalités personnalisées pour charger le module de ressources et charger des ressources spécifiques à partir de celui-ci. Par exemple, si vous utilisez un fichier de ressources .txt ou .xml, l’application doit utiliser un analyseur TXT ou XML pour charger le fichier, puis analyser le contenu du fichier pour chaque ressource requise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation de interface utilisateur multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



