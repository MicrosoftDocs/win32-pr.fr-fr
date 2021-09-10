---
title: Emprunt d'identité
description: L’emprunt d’identité est la capacité d’un thread à s’exécuter dans un contexte de sécurité différent du contexte du processus qui possède le thread.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363404"
---
# <a name="impersonation"></a>Emprunt d'identité

L’emprunt d’identité est la capacité d’un thread à s’exécuter dans un contexte de sécurité différent du contexte du processus qui possède le thread. En cas d’exécution dans le contexte de sécurité du client, le serveur « est » le client, dans une certaine mesure. Le thread serveur utilise un jeton d’accès qui représente les informations d’identification du client pour obtenir l’accès aux objets auxquels le client a accès.

La raison principale de l’emprunt d’identité est de faire en sorte que les vérifications d’accès soient effectuées sur l’identité du client. L’utilisation de l’identité du client pour les vérifications d’accès peut entraîner une restriction ou une extension de l’accès, en fonction de ce que le client est autorisé à faire. Par exemple, supposons qu’un serveur de fichiers possède des fichiers contenant des informations confidentielles et que chacun de ces fichiers soit protégé par une liste de contrôle d’accès. Pour empêcher un client d’obtenir un accès non autorisé aux informations contenues dans ces fichiers, le serveur peut emprunter l’identité du client avant d’accéder aux fichiers.

## <a name="access-tokens-for-impersonation"></a>Jetons d’accès pour l’emprunt d’identité

Les jetons d’accès sont des objets qui décrivent le contexte de sécurité d’un processus ou d’un thread. Ils fournissent des informations qui incluent l’identité d’un compte d’utilisateur et un sous-ensemble des privilèges disponibles pour le compte d’utilisateur. Chaque processus a un *jeton d’accès principal* qui décrit le contexte de sécurité du compte d’utilisateur associé au processus. Par défaut, le système utilise le jeton principal lorsqu’un thread du processus interagit avec un objet sécurisable. Toutefois, lorsqu’un thread emprunte l’identité d’un client, le thread d’emprunt d’identité dispose à la fois d’un jeton d’accès principal et d’un *jeton d’emprunt d’identité*. Le jeton d’emprunt d’identité représente le contexte de sécurité du client, et ce jeton d’accès est celui utilisé pour les vérifications d’accès pendant l’emprunt d’identité. Lorsque l’emprunt d’identité est terminé, le thread revient à utiliser uniquement le jeton d’accès principal.

Vous pouvez utiliser la fonction [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) pour obtenir un handle vers le jeton principal d’un processus. Utilisez la fonction [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) pour obtenir un handle pour le jeton d’emprunt d’identité d’un thread.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jetons d’accès](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Délégation et emprunt d’identité](delegation-and-impersonation.md)
</dt> </dl>

 

 