---
title: Utilisation des extensions NPS
description: En savoir plus sur l’utilisation des extensions NPS. Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Service d’authentification Internet IAS, tâches
- Service d’authentification Internet IAS, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989068"
---
# <a name="using-nps-extensions"></a>Utilisation des extensions NPS

Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server). Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

* * Windows Server 2008 R2 et Windows Server 2008 : * *

Les exemples Dial et MapName étendent les fonctionnalités du serveur NPS.



| Exemple             | Description                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profil<br/>  | Cet exemple implémente une DLL d’extension RADIUS qui vérifie le bit d’accès à distance pour l’utilisateur.<br/>                                                                                                              |
| MapName<br/> | Cet exemple de DLL d’extension recherche le compte désigné dans tous les domaines approuvés. Cela permet aux utilisateurs de plusieurs domaines d’être authentifiés sans que les utilisateurs aient à fournir leur nom de domaine.<br/> |



 

Vous pouvez trouver le code source pour les exemples d’applications MapName et Dial dans la liste suivante. L' *emplacement*% Installation Path%, désigne le répertoire d’installation de base pour les ordinateurs x64. Consultez également le [Kit de développement logiciel (SDK) Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), le kit de développement logiciel (SDK) Microsoft Windows et les [téléchargements pour le développement d’applications du Windows Store](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

SDK Windows pour Windows 8
</dt> <dd>

Windows Server 2012

Lien de téléchargement : N/A

MapName : non

Numérotation : non

Emplacement : N/A

</dd> <dt>

Kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0
</dt> <dd>

Windows Server 2008 R2

Lien de téléchargement : <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName : Oui

Numérotation : non

Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 7.1 \\ \\ netds \\ IAS

</dd> <dt>

Kit de développement logiciel (SDK) Windows
</dt> <dd>

Windows Server 2008

Lien de téléchargement : <https://www.microsoft.com/download/details.aspx?id=5023>

MapName : Oui

Numérotation : non

Emplacement :% installation chemin%% \\ SDK \\ Microsoft \\ exemples Windows v 6.1 \\ \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Téléchargements pour les développeurs](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[SDK Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





