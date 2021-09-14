---
title: Afficher les sons (et l’indicateur de description audio)
description: Cette rubrique contient des informations sur un paramètre qui indique si une application doit fournir une alerte ou un signal visuel quand elle utilise du son pour transmettre des informations importantes.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01e3fda902c23c86279a9a4d75889ebfeff4d55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010623"
---
# <a name="show-sounds-and-audio-description-flag"></a>Afficher les sons (et l’indicateur de description audio)

Cette rubrique contient des informations sur un paramètre qui indique si une application doit fournir une alerte ou un signal visuel quand elle utilise du son pour transmettre des informations importantes. Il fournit également des informations sur un indicateur qui indique si une application doit fournir une description audio pour les éléments visuels.

## <a name="show-sounds-parameter"></a>Afficher le paramètre des sons

Le paramètre show Sounds indique si l’utilisateur souhaite que les applications présentent toutes les informations importantes sous forme visuelle.

L’utilisateur contrôle le paramètre du paramètre afficher les sons à l’aide de la facilité d’accès du panneau de configuration, ou d’une autre application pour la personnalisation de l’environnement. Les applications utilisent les indicateurs **SPI \_ GETSHOWSOUNDS** et **SPI \_ SETSHOWSOUNDS** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre show Sounds. Les applications peuvent également utiliser l’indicateur **du \_ texte du SM** avec la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) pour déterminer l’état du paramètre afficher les sons.

La détermination de l’état du paramètre afficher les sons est nécessaire uniquement pour les applications qui présentent généralement des informations importantes par le biais d’un son seul. Les applications doivent fournir une prise en charge de l’affichage des sons s’ils utilisent des sons de l’une des manières suivantes :

-   Pour transmettre des informations qui sont importantes pour le fonctionnement de l’application.
-   Pour avertir l’utilisateur que des informations importantes sont présentées visuellement. Si c’est le cas, même si les informations sont présentées visuellement, le son a la fonction supplémentaire d’attirer l’attention de l’utilisateur.

Les formulaires de commentaires visuels appropriés peuvent rendre le logiciel bien plus fonctionnel pour les utilisateurs qui ne peuvent pas se baser sur le son seul. La conception des commentaires visuels est spécifique à l’application et dépend des informations qui seront présentées à l’utilisateur. Par exemple, pour attirer l’attention de l’utilisateur quand de nouveaux courriers électroniques arrivent, l’application peut clignoter dans sa fenêtre ou même faire clignoter la totalité de l’écran. Si l’application émet généralement un son pour indiquer que l’utilisateur tente d’effectuer une opération non conforme, elle peut également afficher un message approprié sur sa ligne d’État ou utiliser la fonction [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) pour afficher un message d’erreur spécifique. Si l’application est généralement conçue pour jouer un bruit de son, tel que la reconnaissance vocale numérisée, elle peut également afficher une fenêtre de légende avec le même texte.

L’utilisation redondante des alertes audibles et visuelles a été prouvée pour augmenter la convivialité des applications logicielles. Le paramètre show Sounds est une demande de retour visuel, mais son utilisation ne restreint pas une application à la présentation visuelle des informations. Les utilisateurs doivent pouvoir demander des commentaires visuels, qu’ils aient ou non également des commentaires audibles.

## <a name="audio-description-flag"></a>Indicateur de description audio

Les applications utilisent les indicateurs **SPI \_ GETAUDIODESCRIPTION** et **SPI \_ SETAUDIODESCRIPTION** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour activer ou désactiver les descriptions audio. Bien qu’il soit possible pour les utilisateurs malvoyants d’écouter l’audio dans du contenu vidéo, il y a beaucoup d’actions dans la vidéo qui n’ont pas de son correspondant. Une description audio spécifique de ce qui se passe dans une vidéo permet à ces utilisateurs de mieux comprendre le contenu. Cet indicateur vous permet d’activer ou de désactiver les descriptions audio dans les langues dans lesquelles ils sont fournis.

 

 