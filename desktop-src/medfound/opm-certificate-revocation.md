---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Révocation de certificat OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527891"
---
# <a name="opm-certificate-revocation"></a>Révocation de certificat OPM

Un certificat de sortie Protection Manager (OPM) peut être révoqué par Microsoft. La liste des certificats révoqués est stockée dans une liste de révocation globale (GRL). Le GRL a le format suivant :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Section</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>En-tête</td>
<td>Structure <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contient les listes de révocation suivantes :
<ul>
<li>Révocations binaires du noyau</li>
<li>Révocations binaires en mode utilisateur</li>
<li>Révocations de certificats</li>
<li>Racines de confiance (réservées)</li>
</ul>
La liste des racines de confiance n’est pas utilisée actuellement et est réservée à une utilisation ultérieure.</td>
</tr>
<tr class="odd">
<td>Entrées extensibles</td>
<td>Contient des informations utilisées par d’autres composants. Cette section ne concerne pas OPM.</td>
</tr>
<tr class="even">
<td>Renouvellements</td>
<td>Contient des GUID qui définissent des identificateurs de Windows Update. Cette section contient des identificateurs pour les listes suivantes :
<ul>
<li>Révocations binaires du noyau</li>
<li>Révocations binaires en mode utilisateur</li>
<li>Révocations de certificats</li>
</ul>
Une application peut utiliser ces identificateurs pour demander une version renouvelée d’un binaire révoqué, si celle-ci est disponible.</td>
</tr>
<tr class="odd">
<td>Signature : section principale</td>
<td>Signe l’en-tête et les sections principales.</td>
</tr>
<tr class="even">
<td>Signature : section extensible</td>
<td>Signe l’en-tête et les sections extensibles.</td>
</tr>
</tbody>
</table>



 

L’en-tête GRL est une structure d' [**\_ en-tête GRL**](grl-header.md) . Le membre **dwSequenceNumber** de la structure contient le numéro de version GRL. Ce nombre est incrémenté chaque fois que le GRL est mis à jour et qu’une nouvelle version est placée sur l’ordinateur de l’utilisateur.

Les certificats OPM révoqués sont répertoriés dans la liste de révocation des certificats de la section principale. Chaque entrée de cœur dans le GRL est un tableau de 20 octets qui contient le hachage SHA-1 de la clé publique du certificat révoqué.

Les sections signature contiennent des signatures qui peuvent être utilisées pour vérifier que le GRL n’a pas été falsifié. Chaque section de signature contient la structure de [**\_ signature am MF**](mf-signature.md) . La première signature signe l’en-tête plus la section principale. La deuxième signature signe l’en-tête plus la section extensible ; Cette signature n’est pas pertinente pour OPM.

Pour vous assurer que le GRL lui-même n’a pas été falsifié, vérifiez la signature comme suit :

1.  Recherche le début de la structure de [**\_ signature MF**](mf-signature.md) . L’emplacement de la structure de **\_ signature MF** est indiqué dans le membre **cbSignatureCoreOffset** de la structure d' [**\_ en-tête GRL**](grl-header.md) . L’emplacement est spécifié en tant que décalage en octets à partir du début du GRL.
2.  Analyser la structure de [**\_ signature MF**](mf-signature.md) en tant que \# signature PKCS 7 avec une chaîne de certificats.
3.  Vérifiez la chaîne de certificats jusqu’à une racine approuvée.
4.  Vérifiez que le certificat feuille a l’identificateur d’objet suivant dans l’EKU : « 1.3.6.1.4.1.311.10.5.4 ».
5.  Calculez un hachage des octets qui incluent l’en-tête et les sections principales du GRL.
6.  Vérifiez que le hachage correspond à la signature dans le certificat feuille.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> <dt>

[**\_en-tête GRL**](grl-header.md)
</dt> <dt>

[**\_signature MF**](mf-signature.md)
</dt> </dl>

 

 



