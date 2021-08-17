---
description: Votre DLL de reconnaissance doit être inscrite pour que la plateforme Tablet PC l’utilise. Le module de reconnaissance doit apporter les modifications suivantes au registre lors de l’installation.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Inscription de votre DLL de module de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae80eb49f1795e315cf77bf5aede83cc1677e168f4aea4d6715a216e74434caf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350069"
---
# <a name="registering-your-recognizer-dll"></a>Inscription de votre DLL de module de reconnaissance

Votre DLL de reconnaissance doit être inscrite pour que la plateforme Tablet PC l’utilise. Le module de reconnaissance doit apporter les modifications suivantes au registre lors de l’installation.

Ajoutez une nouvelle clé pour chacun des CLSID de votre module de reconnaissance sous la clé de \_ Registre HKEY local \_ machine/Software/Microsoft/TPG/Recognizers/. Ajoutez un CLSID par langue. Le tableau suivant décrit les valeurs qui doivent être ajoutées sous chacune des clés contenant vos CLSID.

> [!Note]  
> Les noms de ces valeurs respectent la casse.

 



| Nom de la valeur                             | Type de valeur             | Description de la valeur                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indicateurs de fonctionnalité de reconnaissance<br/> | \_valeur DWORD reg<br/>  | Valeur DWORD utilisée pour déterminer les fonctionnalités du module de reconnaissance.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL de reconnaissance<br/>              | SZ de REG \_<br/>     | Chemin d’accès complet à la DLL de reconnaissance installée.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Langues reconnues<br/>        | \_fichier binaire reg<br/> | Tableau binaire décrivant le ou les langages avec lesquels un module de reconnaissance est conçu pour fonctionner.<br/> Dans rectypes. h, la \_ définition Max languages définit spécifie le nombre maximal de langues prises en charge par un module de reconnaissance et chaque langue prend un mot à stocker dans l’élément « langues reconnues ». La taille de l' \_ entrée de Registre reg Binary doit être Max \_ Language \* sizeof (Word).<br/> |



 

 

 




