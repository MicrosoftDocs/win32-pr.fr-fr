---
title: WM/MediaClassSecondaryID
description: L’attribut WM/MediaClassSecondaryID contient le GUID de la classe de support secondaire.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Format Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380903"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

L’attribut **WM/MediaClassSecondaryID** contient le GUID de la classe de support secondaire.

## <a name="global-constant"></a>Constante globale

\_wszWMMediaClassSecondaryID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut doit être défini sur l’une des valeurs du tableau suivant.



| GUID de la classe secondaire                   | Description                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Utilisez pour les fichiers de livre audio.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Utilisez pour les fichiers audio qui contiennent des mots prononcés, mais qui ne sont pas des livres audio. Par exemple, les routines comédie de mise en attente.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Utilisez pour les fichiers audio liés aux actualités.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Utilisez pour les fichiers audio avec la fonction parler afficher le contenu.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Utilisez pour les fichiers vidéo relatifs aux nouvelles.                                                                                                                                                    |
| « D6DE1D88-C77C-4593-BFBC-9C61E8C373E3 » | Utilisez pour les fichiers vidéo contenant des émissions basées sur le Web, des films courts, des codes de fin, etc. Il s’agit de l’identificateur général pour les divertissements vidéo qui ne rentre pas dans une autre catégorie. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Utilisez pour les fichiers audio contenant des clips audio de jeux.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Utilisez pour les fichiers audio contenant des chansons complètes à partir de pistes audio de jeu. Si seule une partie d’une chanson est encodée dans le fichier, utilisez plutôt l’identificateur pour les clips audio du jeu.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Utilisez pour les fichiers vidéo contenant des vidéos musicales.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Utilisez pour les fichiers vidéo contenant une vidéo de démarrage générale.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Utilisez pour les fichiers vidéo contenant des films de caractéristiques.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Utilisez pour les fichiers vidéo contenant des émissions de télévision. Pour les diaporamas basés sur le Web, utilisez l’identificateur plus générique.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Utilisez pour les fichiers vidéo contenant la vidéo d’entreprise. Par exemple, des réunions ou des vidéos de formation enregistrées.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Utilisez pour les fichiers vidéo contenant des vidéos familiales à partir de photographies.                                                                                                                        |



 

Lorsque vous spécifiez un identificateur de classe secondaire, le fichier doit également contenir un attribut d’identificateur de classe primaire.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




