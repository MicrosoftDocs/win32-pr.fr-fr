---
description: Cette rubrique fournit les meilleures pratiques et des suggestions pour valider et dépanner vos implémentations de IWordBreaker et de IStemmer.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Ressources et meilleures pratiques pour la résolution des problèmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8704597f88bdf77e301dcf3f2099c27ad85eae656e3acdcbd6e43c134bb7e43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844489"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Ressources et meilleures pratiques pour la résolution des problèmes

Cette rubrique fournit les meilleures pratiques et des suggestions pour valider et dépanner vos implémentations de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) et de [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) .

Cette rubrique est organisée comme suit :

-   [Bonnes pratiques](#best-practices)
-   [Test de la cohérence des générateurs de formes dérivées](#testing-stemmer-consistency)
-   [Test de l’entrée non valide dans le générateur de formes dérivées](#testing-for-invalid-input-in-the-stemmer)
-   [Test de la cohérence de l’analyseur lexical](#testing-word-breaker-consistency)
-   [Test des entrées non valides dans l’analyseur lexical](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Meilleures pratiques

-   Assurez-vous que le modèle de thread pour les ressources de langue a la valeur « both » dans le registre.
-   Dans la mesure du possible, placez les données de langage dans une ressource de votre DLL plutôt que dans un fichier séparé. Cela simplifie l’installation et la sécurisation de la DLL. En outre, le fait de placer les données de langue dans une ressource permet d’améliorer les performances de ce composant de ressource de langue.
-   Réduisez les ressources système utilisées par les composants de ressource de langue. Par exemple, si chaque instance d’un objet de ressource de langue nécessite un accès en lecture seule à un lexique, envisagez de partager le lexique entre toutes les instances.
-   Envisagez d’utiliser l’analyseur lexical neutre pour gérer du texte qui n’est pas dans la langue ou les paramètres régionaux de votre implémentation de l’analyseur lexical. Cela permet de s’assurer que le texte est traité de manière cohérente dans toutes les langues.
-   Vérifiez tous les codes de retour et retournez-les à partir de fonctions comme [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) et [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext). Si l’indexation échoue, il est important de transmettre l’erreur afin que l’utilisateur soit informé des documents qui ont été indexés.

### <a name="testing-stemmer-consistency"></a>Test de la cohérence des générateurs de formes dérivées

Nous vous recommandons de surveiller les performances d’une implémentation [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) pour des raisons de cohérence dans les conditions suivantes :

-   Le générateur de formes dérivées effectue une exécution cohérente entre plusieurs appels à [**IStemmer :: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init). Le générateur de formes dérivées réinitialise avec les mêmes paramètres que dans l’initialisation précédente, sans libérer les paramètres.
-   À partir du même corping de test et des répétitions de la même requête, [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) produit la sortie identique et effectue des appels identiques aux méthodes de l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Test de l’entrée non valide dans le générateur de formes dérivées

Nous vous recommandons de surveiller la façon dont les méthodes [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) gèrent toutes les erreurs liées aux paramètres non valides. En outre, nous vous recommandons de vous assurer que les méthodes de générateur de formes dérivées ne déclenchent pas d’exceptions non gérées. Le générateur de formes dérivées doit gérer les erreurs suivantes :

-   L’appel à [**IStemmer :: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) avec *pfLicense* a la valeur **null**. Init échoue et n’entraîne pas de violation d’accès.
-   Appelez [**IStemmer :: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) avec le paramètre *ppwcsLicense* défini sur la valeur **null**. **IStemmer :: GetLicenseToUse** n’entraîne pas de violation d’accès.
-   Appelez [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) avec le paramètre *pwcInBuf* défini sur la valeur **null**. **IStemmer :: GenerateWordForms** échoue (retourne E \_ Fail) et n’entraîne pas de violation d’accès.
-   Appelez [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) avec le paramètre *CWC* égal à 0. **IStemmer :: GenerateWordForms** retourne correctement (retourne S \_ OK) et n’entraîne pas de violation d’accès.
-   Appelez [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) avec le paramètre *PwcInBuf* défini sur **null** et le paramètre *CWC* égal à 0. **IStemmer :: GenerateWordForms** échoue (retourne E \_ Fail) et n’entraîne pas de violation d’accès.

### <a name="testing-word-breaker-consistency"></a>Test de la cohérence de l’analyseur lexical

Nous vous recommandons de vous assurer que l’implémentation de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) s’exécute de manière cohérente dans les conditions suivantes :

-   L’analyseur lexical effectue une exécution cohérente entre plusieurs appels à sa méthode [**IWordBreaker :: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) . Le séparateur de mots réinitialise avec les mêmes paramètres que dans l’initialisation précédente, sans libérer les paramètres.
-   À partir du même corping de test et des répétitions de la même requête, la méthode [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) produit la sortie identique et effectue des appels identiques aux méthodes des objets [**IWordSink**](iwordsink.md) et [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) .

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Test des entrées non valides dans l’analyseur lexical

Nous vous recommandons de vous assurer que les méthodes [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) gèrent toutes les erreurs liées aux paramètres non valides. En outre, nous vous recommandons de vous assurer que les méthodes de l’analyseur lexical ne déclenchent pas d’exceptions non gérées. L’analyseur lexical doit exécuter les fonctions suivantes et gérer les erreurs suivantes :

-   L’appel à [**IWordBreaker :: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) doit retourner la \_ \_ base de données langue E \_ \_ introuvable ou S \_ OK.
-   L’appel à [**IWordBreaker :: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) Initialise correctement le paramètre *pfLicense* sur **false** et appelle [**IStemmer :: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) et n’entraîne pas de violation d’accès.
-   L’analyseur lexical ne lit pas au-delà de la fin du paramètre *awcBuffer* dans la méthode [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) .
-   Appelez [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) avec le *pwcInBuf* ayant la valeur **null**. **IWordBreaker :: BreakText** échoue (retourne E \_ Fail) et n’entraîne pas de violation d’accès.
-   Appelez [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) avec le paramètre *CWC* égal à 0. **IWordBreaker :: BreakText** retourne correctement (retourne S \_ OK) et n’entraîne pas de violation d’accès.
-   Appelez la méthode [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) avec le paramètre *pwcInBuf* défini sur la **valeur null** et le paramètre *CWC* égal à 0. **IWordBreaker :: BreakText** échoue (retourne E \_ Fail) et n’entraîne pas de violation d’accès.
-   Les expressions générées pendant la création de l’index contiennent le même nombre de mots.
-   Les expressions sont générées lors de la création d’index via des appels successifs aux méthodes [**IWordFormSink ::P utword**](iwordsink-putword.md) et [**IWordFormSink ::P utaltword**](iwordsink-putaltword.md) . L’analyseur lexical utilise uniquement l’objet [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) au moment de la requête.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Fonctionnement des composants de ressources linguistiques](understanding-language-resource-components.md)
</dt> <dt>

[Implémentation d’un analyseur lexical et du générateur de formes dérivées](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
