---
title: Interfaces IAVIStream et IAVIFile
description: Interfaces IAVIStream et IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interface IAVIStream
- Interface IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007201"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfaces IAVIStream et IAVIFile

Les interfaces [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) et [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contiennent les méthodes utilisées par les gestionnaires de fichiers et de flux. Le type de données **PAVISTREAM** est un pointeur vers un objet de flux AVI (via l’interface **IAVIStream** ) et le type de données **PAVIFILE** est un pointeur vers un objet fichier AVI (via l’interface **IAVIFile** ).

Pour créer un pointeur d’objet en C, commencez par allouer de l’espace pour une structure suffisamment grande pour contenir le pointeur vers la table de fonctions virtuelles et les autres membres de données. Créez une table de fonctions virtuelles pour les méthodes de votre type de flux, puis définissez le pointeur vers la table de fonctions virtuelles sur l’adresse de la table de fonctions virtuelles.

 

 




