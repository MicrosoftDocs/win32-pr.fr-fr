---
title: Accès à la bibliothèque
description: Accès à la bibliothèque
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Lecteur Windows Media, bibliothèque
- Lecteur Windows Media modèle objet, bibliothèque
- modèle objet, bibliothèque
- Lecteur Windows Media Mobile, bibliothèque pour le modèle objet
- Lecteur Windows Media ActiveX contrôle, bibliothèque pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, bibliothèque pour le modèle objet
- contrôle ActiveX, bibliothèque pour le modèle objet
- bibliothèque de Lecteur Windows Media, accès
- bibliothèque, accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295131"
---
# <a name="library-access"></a>Accès à la bibliothèque

les propriétés et les méthodes du modèle objet Lecteur Windows Media qui accèdent à la bibliothèque requièrent un accès en lecture seule ou en lecture/écriture à la base de données. La bibliothèque contient des informations que certains utilisateurs veulent conserver privées et qui doivent être accessibles ou modifiés uniquement avec leur consentement.

pour Lecteur Windows Media série 9 ou version ultérieure, vous pouvez déterminer par programmation le niveau d’accès. pour déterminer le niveau d’accès actuel accordé à votre code, récupérez le *Paramètres*. propriété **mediaAccessRights** . Cette propriété retourne « None », « Read » ou « Full » (lecture/écriture). pour demander des droits d’accès spécifiques, appelez la *Paramètres*. méthode **requestMediaAccessRights** , en passant un paramètre qui spécifie le niveau que vous demandez. La méthode affiche un message à l’utilisateur expliquant le niveau d’accès demandé et retourne une valeur **booléenne** indiquant si l’accès a été accordé.

Certains droits d’accès sont accordés automatiquement en fonction de l’emplacement d’exécution de votre code par rapport à l’ordinateur de l’utilisateur.

-   Si votre page Web ou votre programme se trouve sur l’ordinateur de l’utilisateur, les droits d’accès complets sont accordés par défaut.
-   Les pages Web ont un accès en lecture à *Player*. **currentMedia**, *Player*. **currentPlaylist** et *Media*. **sourceURL** lorsque la page Web se trouve dans une zone de sécurité Internet Explorer qui est identique ou moins restreinte à la zone de sécurité de l’élément multimédia ou de la sélection.

    Du moins limité au plus restreint, les zones de sécurité sont la zone **approuvée** (y compris l’ordinateur local de l’utilisateur), la zone **Intranet local** , la zone **Internet** et la zone **restreinte** .

    Par exemple, une page Web dans la zone **Intranet local** dispose de droits d’accès complets à *Player*. **currentMedia** lorsque l’élément multimédia correspondant se trouve sur l’intranet local ou sur Internet, mais que les droits d’accès doivent être demandés pour les éléments multimédias situés sur l’ordinateur local d’un utilisateur ou sur un site Web dans la zone **approuvée** .

vous devez tester votre application Web ou Windows dans toutes les zones de sécurité qu’elle peut rencontrer. L’application doit être conçue pour gérer correctement le refus d’une demande d’accès.

Lecteur Windows Media versions de modèle objet antérieures à Lecteur Windows Media série 9 n’incluent pas **mediaAccessRights** ou **requestMediaAccessRights**. ces versions antérieures de Lecteur Windows Media permettent à l’utilisateur de définir des niveaux d’accès à l’aide de la boîte de dialogue **Options** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> <dt>

[**Utilisation de la bibliothèque**](working-with-the-library.md)
</dt> </dl>

 

 




