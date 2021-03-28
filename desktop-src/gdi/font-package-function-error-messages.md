---
description: Messages d’erreur de la fonction package de polices
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Messages d’erreur de la fonction package de polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bcf84f92b60351e8375df682de0c3b01c2aa1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114654"
---
# <a name="font-package-function-error-messages"></a>Messages d’erreur de la fonction package de polices

Les valeurs longues suivantes sont retournées par les fonctions de package de polices ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) et [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) lorsque des erreurs sont rencontrées. En cas de réussite des fonctions, la valeur aucune \_ erreur n’est retournée.



| Valeur retournée                   | Valeur | Description                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| AUCUNE \_ erreur                      | 0     | Aucune erreur ne s'est produite.                                                                                               |
| FORMAT d’erreur \_                    | 1006  | Une erreur de format de données d’entrée s’est produite.                                                                             |
| \_générique Err                   | 1 000  | Une erreur s’est produite dans le code générique.                                                                               |
| mémoire de l’erreur \_                       | 1005  | Une erreur s’est produite lors de l’allocation de mémoire.                                                                      |
| ERR \_ aucun \_ glyphe                | 1009  | Aucun glyphe n’a été trouvé.                                                                                            |
| ERREUR \_ de \_ base non valide             | 1085  | La police contenait une table de données de référence (BASE) non valide. Actuellement, cette valeur n’est pas utilisée.                      |
| ERREUR \_ de \_ CMAP non valide             | 1030  | La police contenait une table de mappage de caractères à glyphes (CMAP) non valide.                                           |
| ERR \_ \_ format de Delta non valide \_    | 1013  | Un format Delta non valide a été détecté lors de la tentative de sous-ensemble d’une police de format 1 ou 2.                                |
| ERREUR \_ EBLC non valide \_             | 1086  | La police contenait une table de données d’emplacement de bitmap incorporée (EBLC) non valide.                                        |
| ERREUR \_ GLYF non valide \_             | 1061  | La police contenait une table de données de glyphe non valide (glyf).                                                           |
| ERREUR \_ GDEF non valide \_             | 1083  | La police contenait une table de données de définition de glyphe non valide (GDEF). Actuellement, cette valeur n’est pas utilisée.              |
| ERR \_ objets de stratégie de groupe non valides \_             | 1082  | La police contenait une table de données de positionnement de glyphe non valide (objets de stratégie de groupe). Actuellement, cette valeur n’est pas utilisée.             |
| ERREUR \_ GSUB non valide \_             | 1081  | La police contenait une table de données de substitution de glyphe non valide (GSUB).                                              |
| ERREUR \_ HDMX non valide \_             | 1089  | La police contenait une table de métriques d’appareil horizontale (hdmx) non valide.                                            |
| \_ \_ en-tête Err non valide             | 1062  | La police contenait une table d’en-tête de police (Head) non valide.                                                          |
| ERREUR \_ HHEA non valide \_             | 1063  | La police contenait une table d’en-tête horizontale (hhea) non valide.                                                    |
| ERR \_ non valide \_ HHEA \_ ou \_ VHEA   | 1072  | La police contenait une table d’en-tête horizontale (hhea) non valide ou une table d’en-tête de métriques verticales (vhea) non valide. |
| ERREUR \_ HMTX non valide \_             | 1064  | La police contenait une table de métriques horizontales non valide (hmtx).                                                   |
| ERR \_ non valide \_ HMTX \_ ou \_ VMTX   | 1073  | La police contenait une table de métriques horizontales (hmtx) non valide ou une table de métriques verticales (vmtx) non valide.       |
| ERREUR \_ JSTF non valide \_             | 1084  | La police contenait une table de données de justification non valide (JSTF).                                                   |
| ERREUR \_ LTSH non valide \_             | 1087  | La police contenait une table de données de seuil linéaire non valide (LTSH).                                                |
| ERREUR \_ pour non valide \_              | 1080  | La police était une police TrueType ouverte non valide.                                                                      |
| ERREUR \_ VDMX non valide \_             | 1088  | La police contenait une table de métriques d’appareil verticale (VDMX) non valide.                                              |
| ERREUR \_ Loca non valide \_             | 1065  | La police contenait un index non valide pour la table d’emplacement (Loca).                                                    |
| ERREUR \_ MAXP non valide \_             | 1066  | La police contenait une table de profil maximal (maxp) non valide.                                                      |
| ERREUR \_ de \_ somme de contrôle de fusion non valide \_ | 1010  | Une tentative de fusion des sommes de contrôle pour deux polices d’une police mère différente a échoué.                       |
| \_formats de \_ fusion non valides pour Err \_   | 1010  | Une tentative de fusion des polices avec des formats de DTTF incorrects a échoué.                                          |
| ERR \_ \_ NUMGLYPHS de fusion non valide \_ | 1012  | Une tentative de fusion du nombre de glyphes pour deux polices d’une police mère différente a échoué.            |
| ERR \_ nom non valide \_             | 1067  | Le nom du package de polices ou un nom de police n’est pas valide.                                                                |
| ERREUR \_ de \_ publication non valide             | 1068  | La police contenait une table d’informations PostScript non valide (publication).                                               |
| ERREUR \_ OS2 non valide \_              | 1069  | La police contenait une table non valide du système d’exploitation/2 et des métriques spécifiques à Windows (système d’exploitation/2).                                    |
| ERREUR \_ VHEA non valide \_             | 1070  | La police contenait une table d’en-tête de métriques verticales (vhea) non valide.                                              |
| ERREUR \_ VMTX non valide \_             | 1071  | La police contenait une table de métriques verticales (vmtx) non valide.                                                     |
| ERR \_ \_ index TTC non valide \_       | 1015  | Un index de base zéro (TTC) non valide dans le fichier de police a été passé.                                                 |
| ERREUR \_ de \_ CMAP manquante             | 1030  | La police ne contient pas de table CMAP.                                                                           |
| ERREUR \_ EBDT manquante \_             | 1044  | La police ne contient pas de table EBDT.                                                                          |
| ERREUR \_ GLYF manquante \_             | 1031  | La police ne contient pas de table glyf.                                                                           |
| ERR \_ manquant \_             | 1032  | La police ne contient pas de table des en-têtes.                                                                           |
| ERREUR \_ HHEA manquante \_             | 1033  | La police ne contient pas de table hhea.                                                                          |
| ERREUR \_ HMTX manquante \_             | 1034  | La police ne contient pas de table hmtx.                                                                          |
| ERREUR \_ Loca manquante \_             | 1035  | La police ne contient pas de table Loca.                                                                           |
| ERREUR \_ MAXP manquante \_             | 1036  | La police ne contient pas de table maxp.                                                                           |
| ERR \_ - \_ nom manquant             | 1037  | La police ne contient pas de table de noms (Name).                                                                  |
| ERREUR \_ de \_ publication manquante             | 1038  | La police ne contient pas de table de publication.                                                                           |
| ERREUR de \_ OS2 absente \_              | 1039  | La police ne contient pas de table OS/2.                                                                          |
| ERREUR \_ VHEA manquante \_             | 1040  | La police ne contient pas de table vhea.                                                                           |
| ERREUR \_ VMTX manquante \_             | 1041  | La police ne contient pas de table vmtx.                                                                           |
| ERREUR \_ \_ HHEA \_ ou \_ VHEA manquant   | 1042  | La police ne contient pas de table hhea ou de table vhea.                                                          |
| ERREUR \_ \_ HMTX \_ ou \_ VMTX manquant   | 1043  | La police ne contient pas de table hmtx ou de table vmtx.                                                          |
| ERR \_ non \_ TTC                  | 1014  | La valeur fournie n’est pas un index pour un fichier TTC.                                                              |
| ERREUR \_ PARAMETER0                | 1100  | Le paramètre de fonction d’appel 0 n’était pas valide.                                                                        |
| ERREUR \_ paramètre1                | 1101  | Le paramètre de fonction 1 appelant n’était pas valide.                                                                        |
| ERREUR \_ paramètre2                | 1102  | Le paramètre de fonction 2 appelant n’était pas valide.                                                                        |
| ERREUR \_ paramètre3                | 1103  | Le paramètre de fonction d’appel 3 n’était pas valide.                                                                        |
| ERREUR \_ paramètre4                | 1104  | Le paramètre de fonction 4 appelant n’était pas valide.                                                                        |
| ERREUR \_ PARAMETER5                | 1105  | Le paramètre de fonction 5 appelant n’était pas valide.                                                                        |
| ERREUR \_ PARAMETER6                | 1106  | Le paramètre de fonction d’appel 6 n’était pas valide.                                                                        |
| ERREUR \_ PARAMETER7                | 1107  | Le paramètre de fonction d’appel 7 n’était pas valide.                                                                        |
| ERREUR \_ PARAMETER8                | 1108  | Le paramètre de fonction d’appel 8 n’est pas valide.                                                                        |
| ERREUR \_ PARAMETER9                | 1109  | Le paramètre de fonction 9 appelant n’était pas valide.                                                                        |
| ERREUR \_ PARAMETER10               | 1110  | Le paramètre de fonction 10 appelant n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER11               | 1111  | Le paramètre de fonction 11 appelant n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER12               | 1112  | Le paramètre de fonction 12 appelant n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER13               | 1113  | Le paramètre de fonction 13 appelant n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER14               | 1114  | Le paramètre de fonction appelant 14 n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER15               | 1115  | Le paramètre de fonction 15 appelant n’était pas valide.                                                                       |
| ERREUR \_ PARAMETER16               | 1116  | Le paramètre de fonction d’appel 16 n’était pas valide.                                                                       |
| ERREUR \_ READCONTROL               | 1003  | La structure de contrôle de lecture ne correspondait pas aux données.                                                                   |
| ERREUR \_ READOUTOFBOUNDS           | 1001  | Une lecture à partir de la mémoire n’était pas autorisée, peut-être parce que les données sont hors limites ou endommagées.                          |
| VERSION d’ERR \_                   | 1008  | La valeur principale DTTF. version des données d’entrée est supérieure à la version que la fonction peut lire.                   |
| l’erreur \_ peut \_ croître               | 1007  | L’action demandée a entraîné une croissance des données et l’application doit utiliser les données d’origine.                             |
| ERREUR \_ WRITECONTROL              | 1004  | La structure de contrôle d’écriture ne correspondait pas aux données.                                                                  |
| ERREUR \_ WRITEOUTOFBOUNDS          | 1002  | L’écriture dans la mémoire n’était pas autorisée, peut-être parce que les données étaient hors limites.                                      |



 

 

 



