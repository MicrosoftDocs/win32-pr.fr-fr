---
title: Obtention d’un magasin de musique en ligne sur un tableau
description: Obtention d’un magasin de musique en ligne sur un tableau
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player Online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c5d13e14e95e88e83d42fd7d5cd00551bb507
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940173"
---
# <a name="getting-an-online-music-store-on-board"></a>Obtention d’un magasin de musique en ligne sur un tableau

Cette rubrique décrit le processus de mise en ligne d’un magasin de médias numériques en ligne pour le lecteur Windows Media. Le temps nécessaire pour que le processus d’intégration commence à se terminer est d’environ 45-60 jours OUVRABLEs. Les deux étapes du processus d’intégration sont décrites dans le tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Étape</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pending</td>
<td><ul>
<li>Vous envoyez à Microsoft les informations de contact, les informations de démarrage et les comptes de validation requis.</li>
<li>Microsoft vous envoie une clé de test et une clé de production.</li>
<li>Vous testez votre boutique en ligne avec le lecteur Windows Media.</li>
<li>Vous soumettez des contrats et contrats signés à Microsoft.</li>
</ul></td>
</tr>
<tr class="even">
<td>Validation</td>
<td>Microsoft valide votre magasin en ligne.</td>
</tr>
</tbody>
</table>



 

Une fois que vous avez terminé les étapes en attente et de validation, Microsoft publiera votre boutique en ligne.

## <a name="pending-stage"></a>Étape en attente

L’étape en attente vous donne la possibilité de tester votre boutique en ligne dans le lecteur Windows Media. Il est également judicieux de s’assurer que tous les contrats et contrats requis sont signés. Pour commencer, envoyez les informations suivantes à Microsoft, comme défini plus loin dans cette rubrique :

-   Informations de contact
-   Informations de démarrage
-   Comptes de validation

Lors de la réception de vos informations de contact et de démarrage, Microsoft vous enverra une clé de test et une clé de production. Une fois que vous avez ajouté votre clé de test au registre et redémarré le lecteur, votre magasin en ligne s’affiche dans le lecteur et vous pouvez le tester. Pour plus d’informations sur l’emplacement de votre clé de test dans le registre, consultez [clés et entrées de Registre pour un magasin en ligne de type 1](registry-keys-and-entries-for-a-type-1-online-store.md) ou des [clés de Registre et des entrées pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).

Vous devez tester tous les aspects de votre boutique en ligne, y compris son interface utilisateur et son plug-in. Dans le cadre de votre processus de test, vous devez exécuter les tests décrits dans [tests de validation pour les magasins de musique de type 2 en ligne](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Les magasins de type 1 doivent réussir tous les tests de validation pour les magasins de type 2 et certains tests supplémentaires qui sont spécifiques à l’expérience de type 1. Pour plus d’informations sur les tests de validation de type 1, contactez l’équipe virtuelle des services de lecteur Windows Media à l’adresse mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Informations de contact

Le tableau suivant présente les informations de contact dont Microsoft a besoin pour votre boutique en ligne. Remplissez le [formulaire d’informations de contact](contact-information-form-for-an-online-music-store.md) et envoyez-le à l’équipe virtuelle des services de lecteur Windows Media à l’adresse mpsvctm@microsoft.com .



| Élément                     | Description                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Store Name               | Nom de votre boutique                                                            |
| Nom du fournisseur            | Nom de la société du fournisseur/de l’étiquette blanche (si différente)                               |
| Paramètres régionaux du Store             | Les paramètres régionaux utilisateur Windows sur lesquels votre magasin doit s’afficher                                |
| Catégorie de magasin           | Musique, radio, film, TV, sports, Actualités, divertissement audio et/ou autre (à décrire) |
| Modèle d’achat           | Achat, location, abonnement et/ou autre (à préciser)                            |
| Langue du magasin           |                                                                                           |
| Stocker le (s) nom (s) du contact    |                                                                                           |
| Stocker le ou les courriers électroniques des contacts  |                                                                                           |
| Compte (s) Passport MSFT | C’est le cas pour des nominations futures possibles dans les programmes de développement bêta et partenaire.         |
| Adresse de livraison         | Aucune postale Zones                                                                             |
| City                     |                                                                                           |
| State                    |                                                                                           |
| Code postal              |                                                                                           |
| Pays/région           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contact de l’enquête           | Est-il possible si nous vous contacterons avec le programme à l’avenir ?        |



 

## <a name="startup-information"></a>Informations de démarrage

Pour chaque région géographique que votre magasin va servir, envoyez à Microsoft un ensemble d’informations de démarrage pour votre magasin de tests, un ensemble d’informations de démarrage pour votre magasin de production et un ensemble de comptes de validation.

Le [formulaire d’informations de démarrage de la rubrique pour un magasin de musique en ligne](startup-information-form-for-an-online-music-store.md) contient deux copies du formulaire d’informations de démarrage et une copie du formulaire comptes de validation. Remplissez les formulaires et envoyez-les à l’équipe virtuelle des services de lecteur Windows Media à l’adresse mpsvctm@microsoft.com .

Le tableau suivant décrit les informations de démarrage dont Microsoft a besoin pour votre magasin en ligne.



| Élément                                                                                                     | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL XML des informations de service (2048-limite de caractères)                                                              | URL où le lecteur Windows Media obtient votre [document XML serviceInfo](serviceinfo-document.md).                                                                                                                                         |
| Clé de service (ID unique)                                                                                  | Chaîne qui identifie de façon unique votre magasin en ligne. Vous devez en créer un pour la production et un pour les tests (par exemple, « MyStore » et « MyStoreTest »). Notez qu’une clé de service n’est pas la même chose qu’une clé de test.                        |
| Nom convivial (30 caractères maximum)                                                                       | Nom de votre magasin affiché dans le sélecteur de service du lecteur Windows Media.                                                                                                                                                        |
| URL de l’image de menu (2048-limite de caractères)                                                                    | URL où le lecteur Windows Media récupère le logo de 15 x 15 pixels qu’il affiche dans le sélecteur de service.                                                                                                                                 |
| Acheter une URL musicale (2048 caractères maximum)<br/> (Magasins de musique intégrés uniquement)<br/>                | URL qui est utilisée par les liens « acheter un CD » et « acheter à la musique en ligne » du lecteur.                                                                                                                                                              |
| URL d’achat 10 ft UI (2048 caractères maximum)<br/> (Magasins de musique intégrés uniquement--facultatif)<br/> | L’URL qui est utilisée par les liens « acheter un CD » et « acheter à la musique en ligne » du lecteur dans Windows XP Media Center Edition et dans Windows Media Center dans Windows Vista.                                                                              |
| Logo de la boutique (130W x sur 30 h)<br/> (Joindre le fichier PNG séparément.)<br/>                              | Logo de la boutique affiché dans l’info-bulle qui s’affiche lorsque la souris se trouve sur l’image parcourir tout. Ce logo doit être un fichier au format PNG et, de préférence, être mélangé en caractères alphanumériques afin qu’il puisse s’adapter aux changements de couleur dans le lecteur Windows Media. |
| Parcourir-All image (108W x 108h)<br/> (Joindre le fichier PNG séparément.)<br/>                       | Brève description dans l’info-bulle qui s’affiche lorsque la souris se trouve sur votre image parcourir tout.                                                                                                                                               |
| Texte de description de la boutique (110 caractères maximum)                                                             | Texte qui apparaît dans l’info-bulle sous le texte de description du magasin.                                                                                                                                                                        |
| Texte pour le lien hypertexte (45 caractères maximum)                                                                  | Logo de la boutique affiché dans la page parcourir tous les magasins en ligne. Il doit s’agir d’un fichier au format PNG et, de préférence, d’un fichier au format alphanumérique, afin qu’il puisse s’adapter aux modifications de couleur dans le lecteur Windows Media.                                           |



 

> [!Note]  
> L’image de recherche de pixels 108 x 108 est requise pour le lecteur Windows Media 11 et les versions ultérieures.

 

> [!Note]  
> Dans le lecteur Windows Media 11 et les versions ultérieures, les éléments ServiceTask2 et ServiceTask3 du document XML ServiceInfo sont ignorés. Pour plus d’informations sur le document XML ServiceInfo, voir le [document serviceInfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Comptes de validation

Pour terminer le processus de validation décrit dans la section étape de validation qui suit, Microsoft requiert cinq (5) comptes de validation pour chaque type de compte que votre magasin en ligne propose. Par exemple, si vous proposez des comptes qui différencient les fonctionnalités et les fonctionnalités, telles que Basic et Premium, Microsoft aura besoin de cinq (5) comptes de validation pour chaque type, pour un total de dix (10) comptes.

Envoyez le nom d’utilisateur et le mot de passe de chaque compte de validation à mpsvctm@microsoft.com . Incluez également le nom d’une personne que Microsoft peut contacter en ce qui concerne les comptes de validation. Ces comptes seront utilisés pour la validation mensuelle continue. Veuillez donc inclure un processus de « rechargement » des comptes. L’un des problèmes les plus courants se produit lorsqu’un magasin en ligne ne parvient pas à fournir un crédit d’achat suffisant pour permettre à Microsoft de valider tous les scénarios d’achat. Les comptes doivent rester actifs une fois le processus d’intégration terminé.

## <a name="validation-stage"></a>Étape de validation

Au cours de l’étape de validation, Microsoft vérifie que les fonctionnalités principales de votre boutique en ligne fonctionnent correctement. Pour tous les magasins (type 1 et type 2), Microsoft exécute les tests de vérification détaillés dans les [tests de validation pour les magasins de musique de type 2 en ligne](validation-tests-for-type-2-online-music-stores.md). Microsoft exécute également des tests de validation supplémentaires pour les magasins de type 1. Si vous avez des questions sur l’étape de validation pour les magasins de type 1, envoyez un e-mail à mpsvctm@microsoft.com .

Au cours de l’étape de validation, Microsoft effectue deux passes de validation. La première passe s’applique à la version Release Candidate 1 (RC1) de votre magasin en ligne. Si votre magasin réussit la validation RC1, vous devez le verrouiller et ne pas apporter de modifications supplémentaires. Microsoft effectuera une deuxième passe de validation sur votre magasin, même si votre magasin réussit la validation RC1.

Si votre magasin ne fait pas partie de l’étape de validation RC1, vous aurez deux semaines pour créer une deuxième version finale candidate (RC2), que Microsoft validera pendant le test de validation RC2.

Si votre magasin échoue à une partie de la validation RC2, vous devez attendre le lancement suivant.

## <a name="test-and-production-keys"></a>Clés de test et de production

Rappelez-vous que, pendant la phase en attente, vous avez envoyé à Microsoft deux jeux d’informations de démarrage : une pour votre magasin de test et une pour votre magasin de production. Souvenez-vous également que Microsoft vous a envoyé deux clés : une clé de test et une clé de production.

La clé de test est entièrement destinée à votre propre utilisation. Lorsque votre clé de test se trouve dans le registre, le lecteur Windows Media utilise l’URL ServiceInfo que vous avez envoyée pour votre magasin de tests.

Lorsque votre clé de production se trouve dans le registre, le lecteur Windows Media utilise l’URL ServiceInfo que vous avez envoyée pour votre magasin de production. Microsoft utilise votre clé de production pendant l’étape de validation. Microsoft n’utilise jamais votre clé de test pour la validation.

Lorsque votre magasin est en ligne, le lecteur Windows Media utilise l’URL ServiceInfo que vous avez envoyée pour votre magasin de production.

En règle générale, votre magasin de test doit être l’endroit où vous développez votre service et apportez des modifications quotidiennes. Votre magasin de production doit être l’endroit où vous gardez une version stable de votre service.

## <a name="common-on-boarding-problems"></a>Problèmes courants liés à l’intégration

Voici quelques problèmes courants qui peuvent entraîner l’échec du test de validation de votre magasin.

-   Échec de la transition des serveurs de test vers les serveurs de production. Cela génère de nombreux problèmes tels que les pages manquantes, les paramètres IIS et de sécurité non valides et les comptes de test qui ne fonctionnent plus.
-   Le lien d’achat (ou lien d’achat) dans la zone de jeu en cours n’est pas valide. Cela peut provoquer l’échec de la validation de votre magasin même lorsque tout le reste fonctionne.
-   L’équipe de validation de Microsoft testera plusieurs scénarios d’achat allant des petits achats à des achats très importants. Vous devez fournir un moyen de refacturation pour qu’ils jouent le rôle de consommateur dans votre magasin. Votre magasin ne peut pas être validé si l’équipe de validation ne dispose pas de crédits d’achat suffisants pour valider tous ces scénarios.

Pour obtenir une liste plus complète des problèmes d’intégration courants et des questions fréquemment posées compilées par l’équipe virtuelle des services de lecteur Windows Media, consultez [problèmes courants liés aux magasins musicaux en ligne](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Kit de bienvenue des magasins en ligne](online-stores-welcome-kit.md)
</dt> </dl>

 

 





