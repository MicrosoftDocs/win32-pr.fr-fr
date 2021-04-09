---
description: Pktextract.exe est un outil qui extrait l’attribut publicKeyToken à partir d’un fichier de certificat.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115186"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe est un outil qui extrait l’attribut **PublicKeyToken** à partir d’un fichier de certificat. La sortie est **PublicKeyToken**, qui est un identificateur unique de 16 caractères (8 octets) de la clé publique présente dans le certificat, dans un format qui peut être facilement collé dans une instruction d’identité d’assembly. Le fichier de certificat doit être présent dans le même répertoire que Pktextract.exe pour pouvoir utiliser l’utilitaire. Pktextract.exe est fourni dans le kit de développement logiciel (SDK) Microsoft Windows.

## <a name="syntax"></a>Syntaxe

**pktextract.exe** *<filename. cer>* **\[ -Quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Options de la ligne de commande

Pktextract.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.



| Option  | Description                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Supprime l’affichage complet des informations de certificat. Optionnel.        |
| -nologo | S’exécute sans afficher les données de copyright Microsoft standard. Optionnel. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement d’assembly côte à côte](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



