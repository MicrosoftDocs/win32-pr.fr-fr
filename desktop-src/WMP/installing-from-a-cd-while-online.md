---
title: Installation à partir d’un CD-ROM en ligne
description: Installation à partir d’un CD-ROM en ligne
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online stores, installation à partir du CD-ROM en ligne
- magasins en ligne, installation à partir du CD-ROM en ligne
- tapez 1 magasins en ligne, installation à partir du CD-ROM en ligne
- tapez 2 magasins en ligne, installation à partir du CD-ROM en ligne
- Windows Media Player Online stores, installations en ligne à partir du CD
- magasins en ligne, installations en ligne à partir du CD
- tapez 1 magasins en ligne, installations en ligne à partir du CD
- type 2 magasins en ligne, installations en ligne à partir du CD
- Windows Media Player Online stores, CD s’installe en ligne
- magasins en ligne, CD-ROM s’installe en ligne
- tapez 1 magasins en ligne, CD installions en ligne
- tapez 2 magasins en ligne, CD installions en ligne
- installation de magasins en ligne à partir d’un CD en ligne
- Installation à partir de CD de magasins en ligne en ligne
- installations en ligne de magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532031"
---
# <a name="installing-from-a-cd-while-online"></a>Installation à partir d’un CD-ROM en ligne

Les utilisateurs peuvent installer le lecteur Windows Media à partir d’un CD tout en étant connecté à Internet. Dans ce cas, le programme d’installation de Windows Media Player localise le document ServiceInfo spécifié par le paramètre de ligne de commande *serviceInfo* . Si l’attribut de **clé** correspond au paramètre de ligne de commande *DefaultService* , le programme d’installation inspecte l’élément d’installation pour personnaliser le processus d’installation. À l’aide des valeurs d’attribut, le programme d’installation affiche votre contrat de licence utilisateur final (CLUF) et votre déclaration de confidentialité, et récupère et installe également votre fichier. cab sur l’ordinateur de l’utilisateur. Par exemple, vous pouvez utiliser cette fonctionnalité pour installer la dernière version d’un objet COM requis par votre magasin en ligne.

Une fois installé, le lecteur Windows Media définit le magasin en ligne initial à l’aide du nom de clé que vous avez spécifié pour le paramètre de ligne de commande *DefaultService* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Élément d’installation**](install-element.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Définition de la boutique en ligne initiale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Paramètres de ligne de commande d’installation pour les magasins en ligne**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




