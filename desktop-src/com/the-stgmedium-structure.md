---
title: La structure STGMEDIUM
description: La structure STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221676"
---
# <a name="the-stgmedium-structure"></a>La structure STGMEDIUM

tout comme la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) est une amélioration de l’identificateur de format du presse-papiers Windows, la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) est une amélioration du descripteur de mémoire globale utilisé pour transférer les données. La structure **STGMEDIUM** inclut un membre, **TYMED**, qui indique le support à utiliser, et une Union comprenant des pointeurs et un handle pour obtenir le support spécifié dans **TYMED**.

La structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permet aux sources de données et aux consommateurs de choisir le support Exchange le plus efficace pour chaque rendu. Si les données sont tellement volumineuses qu’elles doivent être conservées sur le disque, la source de données peut indiquer un support sur disque dans son format préféré, en utilisant uniquement la mémoire globale comme sauvegarde uniquement si c’est le seul moyen que le consommateur comprend. La possibilité d’utiliser le meilleur moyen pour les échanges comme par défaut améliore les performances globales d’échange de données entre les applications. Par exemple, si certaines des données à transférer sont déjà sur le disque, l’application source peut les déplacer ou les copier vers une nouvelle destination, soit dans la même application, soit dans d’autres, sans avoir à charger les données dans la mémoire globale. À l’extrémité de réception, le consommateur des données n’a pas à les réécrire sur le disque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats de données et média de transfert](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




