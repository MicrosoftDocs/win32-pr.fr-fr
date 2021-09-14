---
description: Codes d’erreur et de réussite du streaming multimédia
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Codes d’erreur et de réussite du streaming multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223321"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Codes d’erreur et de réussite du streaming multimédia

> [!Note]  
> Cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

La liste suivante contient des messages d’erreur et des notifications de réussite pour les applications qui utilisent les interfaces de diffusion multimédia en continu. Cette liste ne contient pas toutes les erreurs possibles. les erreurs indiquées s’appliquent spécifiquement à l’implémentation Microsoft® DirectShow® des interfaces de diffusion multimédia en continu.



| Valeur                       | Code hexadécimal | Description                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ en attente              | 0x00040001       | L’exemple de mise à jour n’est pas encore terminé.                                                                                                                                                         |
| MS \_ S \_ noupdate             | 0x00040002       | L’exemple n’a pas été mis à jour après l’achèvement forcé.                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | Fin du flux. Exemple non mis à jour.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Impossible de supprimer un objet [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) d’un objet [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) , car il contient toujours au moins un échantillon alloué. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | L’ID d’objectif spécifié ne peut pas être utilisé pour l’appel.                                                                                                                                       |
| \_E- \_ flux MS E             | 0x80040403       | Aucun flux ne peut être trouvé avec les attributs spécifiés.                                                                                                                                      |
| MS \_ E \_ noseek            | 0x80040404       | Recherche non prise en charge pour cet objet [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) .                                                                                                      |
| MS \_ E \_ incompatible         | 0x80040405       | Les formats de flux ne sont pas compatibles.                                                                                                                                                     |
| MS \_ E \_ occupé                 | 0x80040406       | L’exemple est occupé.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | L’objet ne peut pas accepter l’appel, car sa fonction Initialize ou son équivalent n’a pas été appelé.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Source déjà définie.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | Le type de flux n’est pas valide pour cette opération.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | L’objet [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) n’est pas à l’État en cours d’exécution.                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Diffusion multimédia en continu](multimedia-streaming.md)
</dt> </dl>

 

 



