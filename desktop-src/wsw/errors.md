---
title: Erreurs
description: Cette section décrit les erreurs qui peuvent être des problèmes des fonctions des services Web Windows en raison d’un échec d’exécution de la commande.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Erreurs Web services pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839582"
---
# <a name="errors"></a>Erreurs

Cette section décrit les erreurs qui peuvent être des problèmes des fonctions des services Web Windows en raison d’un échec d’exécution de la commande.

-   [Paramètres de sortie](#out-parameters)
-   [Codes d’erreur](#error-codes)
-   [Erreurs riches](#rich-errors)
-   [Erreurs et Erreurs](#faults-and-errors)
-   [Informations sur l’erreur sensible à la langue](#language-sensitive-error-information)
-   [Codes d’erreur canoniques](#canonical-error-codes)
-   [Utilisation d’API non valide](#invalid-api-usage)
-   [Sécurité](#security)

## <a name="out-parameters"></a>Paramètres de sortie

En règle générale, la valeur des paramètres de sortie n’est pas modifiée si une fonction échoue.

Il existe quelques cas où les paramètres out sont modifiés si la fonction échoue. Ces cas sont appelés explicitement dans la documentation pour chaque paramètre. Si la documentation ne mentionne rien sur la modification des paramètres en cas d’échec, vous pouvez supposer que la fonction ne les modifiera pas.

## <a name="error-codes"></a>Codes d’erreur

Tous les codes de retour d’erreur sont des HRESULT. Cette API définit un jeu de valeurs HRESULT dans la \_ plage de WebServices de la fonction, mais retourne également les erreurs définies ailleurs dans l’API Windows.

Pour en savoir plus sur les codes d’erreur retournés, reportez-vous à la documentation des API spécifiques. La liste n’est pas destinée à être exhaustive pour chaque API, mais plutôt à une liste de codes d’erreur pour lesquels il existe des scénarios courants de gestion explicite. Un appelant doit toujours supposer qu’un autre code d’erreur est possible à partir de n’importe quelle API.

Cette API définit un nombre relativement faible de codes d’erreur, qui correspondent aux scénarios dans lesquels un programme souhaite exécuter une action en fonction de l’erreur. Les codes d’erreur seuls peuvent ne pas suffire pour déterminer la cause du problème ou pour fournir une bonne description du problème à l’utilisateur. La meilleure compréhension du problème provient de l’utilisation d’erreurs riches, comme décrit ci-dessous.

## <a name="rich-errors"></a>Erreurs riches

En plus de retourner un code d’erreur, un appelant peut éventuellement demander des informations complètes sur l’erreur pour tout appel d’API en passant un objet [WS \_](ws-error.md) non **null**. Pour créer un objet d’erreur, utilisez [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). En cas d’erreur, l’API à l’origine de l’erreur remplira l’objet d’erreur avec un contexte supplémentaire sur la situation de l’erreur. S’il n’y a pas d’erreur, l’objet d’erreur n’est pas modifié. Le passage d’un objet d’erreur **null** indique que l’appelant ne s’intéresse pas aux informations d’erreur enrichies. Les appelants (y compris les rappels) doivent être préparés pour gérer les objets d’erreur **null** .

Notez que le même objet d’erreur peut être utilisé pour plusieurs appels d’API, mais ne peut être utilisé que pour un appel d’API à la fois (car il s’agit d’un thread unique). Chaque fois qu’une erreur se produit, les informations d’erreur sont ajoutées à l’objet d’erreur. À mesure qu’une chaîne d’appel se déroule, plusieurs fonctions peuvent ajouter des informations à l’objet d’erreur pour fournir un contexte supplémentaire sur l’erreur. Pour effacer le contenu de l’objet d’erreur avant de le réutiliser (une fois qu’une erreur se produit), utilisez [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Si aucune erreur ne se produit, il n’est pas nécessaire de réinitialiser l’objet d’erreur avant de le réutiliser.

Les informations d’erreur détaillées sont les suivantes :

-   Ensemble de valeurs de propriété, qui fournissent des informations supplémentaires sur l’erreur, le cas échéant. Consultez [**la \_ \_ propriété WS Error**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Zéro, une ou plusieurs chaînes d’erreur. Les chaînes sont ajoutées à l’aide de [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)et peuvent être interrogées à l’aide de [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). Le nombre de chaînes peut être interrogé à l’aide du [**nombre de chaînes de \_ propriétés d’erreur \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Erreurs et Erreurs

Pour plus d’informations sur la relation entre les erreurs et les erreurs, consultez [Erreurs](faults.md) .

## <a name="language-sensitive-error-information"></a>Informations sur l’erreur sensible à la langue

Lors de la création d’un objet d’erreur, l’ID de langue de la traduction de langage souhaitée pour les informations d’erreur est spécifié. Cette valeur est utilisée lors de l’ajout d’informations d’erreur à l’objet d’erreur.

Cette valeur de langue peut être extraite ou définie à l’aide de l' [**\_ ID de \_ propriété \_ WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Codes d’erreur canoniques

Cette API fournit un ensemble canonique de codes d’erreur (WS \_ E \_ \* ) qui permet d’utiliser différentes technologies de communication sans avoir à dépendre des codes d’erreur spécifiques de l’implémentation sous-jacente spécifique. Pour obtenir la liste complète de ces codes d’erreur, consultez [valeurs de retour des services Web Windows](windows-web-services-return-values.md).

Cela permet, par exemple, à un programme de rechercher le code d' **erreur \_ WS \_ E \_ Endpoint \_ introuvable** , si vous utilisez TCP, UDP ou http, et d’effectuer une action (comme tenter d’utiliser un autre point de terminaison).

Lorsqu’un code d’erreur spécifique à l’implémentation est mappé à une erreur canonique, le code d’erreur d’origine est enregistré dans l’objet d’erreur et est toujours accessible à des fins de diagnostic. Pour plus d’informations, consultez [**\_ \_ \_ \_ \_ code d’erreur d’origine de la propriété WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) .

## <a name="invalid-api-usage"></a>Utilisation d’API non valide

Les codes d’erreur suivants sont réservés à l’utilisation d’API non valides et ne sont pas retournés dans d’autres circonstances. Si l’une de ces erreurs est retournée, elle peut indiquer un bogue dans l’application.

-   **\_ \_ opération non valide ws E \_**
-   **E \_ INVALIDARG**

Les énumérations suivantes font partie du suivi :

-   [**\_ID de \_ propriété d’erreur WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_code d’exception WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Les codes d’erreur suivants font partie du suivi :

-   **CERT \_ E \_ CN \_ no \_ match**
-   **CERTIFICAT \_ E \_ expiré**
-   **CERTIFICAT \_ E \_ UNTRUSTEDROOT**
-   **CERTIFICAT \_ E- \_ utilisation incorrecte \_**
-   **CRYPTer la \_ \_ révocation E \_ hors connexion**
-   **E \_ INVALIDARG**
-   **\_OUTOFMEMORY E**
-   **\_adresse WS \_ E \_ en cours d' \_ utilisation**
-   **\_adresse WS \_ E \_ non \_ disponible**
-   **\_ \_ accès au point de terminaison WS E \_ \_ refusé**
-   **\_action de point de terminaison WS E \_ \_ \_ non \_ prise en charge**
-   **\_point de \_ terminaison WS E \_ déconnecté**
-   **\_échec du \_ point de terminaison WS E \_**
-   **\_erreur de \_ point de terminaison WS E \_ \_ reçue**
-   **\_point de terminaison WS E \_ \_ non \_ disponible**
-   **\_point de terminaison WS E \_ \_ \_ introuvable**
-   **\_point de \_ terminaison WS E \_ encombré \_**
-   **\_point de terminaison WS E \_ \_ inaccessible**
-   **\_URL de point de terminaison WS E \_ non valide \_ \_**
-   **\_ \_ format non valide ws E \_**
-   **\_ \_ opération non valide ws E \_**
-   **WS \_ E \_ non \_ pris en charge**
-   **WS \_ E \_ aucune \_ traduction \_ disponible**
-   **\_ \_ dépassement numérique WS \_ E**
-   **\_objet WS \_ E \_ défaillant**
-   **\_opération WS \_ E \_ abandonnée**
-   **\_opération WS \_ E \_ abandonnée**
-   **expiration du délai de l' \_ opération WS E \_ \_ \_**
-   **\_autre WS E \_**
-   **\_ \_ accès proxy WS \_ E \_ refusé**
-   **\_échec du \_ proxy WS E \_**
-   **le \_ proxy WS E \_ \_ requiert l' \_ authentification de base \_**
-   **le \_ proxy WS E \_ \_ requiert l' \_ \_ authentification Digest**
-   **le \_ proxy WS E \_ \_ requiert l' \_ \_ authentification Negotiate**
-   **le \_ proxy WS E \_ \_ requiert l' \_ \_ authentification NTLM**
-   **\_quota WS \_ E \_ dépassé**
-   **\_défaillance du \_ système de sécurité WS E \_ \_**
-   **le \_ jeton de sécurité WS E \_ \_ \_ a expiré**
-   **\_échec de \_ vérification de sécurité WS E \_ \_**
-   **le \_ serveur WS E \_ \_ requiert l' \_ authentification de base \_**
-   **le \_ serveur WS E \_ \_ requiert l' \_ \_ authentification Digest**
-   **le \_ serveur WS E \_ \_ requiert l' \_ \_ authentification Negotiate**
-   **le \_ serveur WS E \_ \_ requiert l' \_ \_ authentification NTLM**
-   **WS \_ S \_ Async**
-   **fin de WS \_ S \_**

Les fonctions suivantes font partie du suivi :

-   [**\_ID de \_ propriété d’erreur WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_code d’exception WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Le handle suivant fait partie du suivi :

-   [\_erreur WS](ws-error.md)

La structure suivante fait partie du suivi :

-   [**WS \_ Error ( \_ propriété)**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Sécurité

L’utilisateur de l’objet d’erreur doit connaître un certain nombre de considérations relatives à la sécurité :

-   L’objet Error peut contenir des données non fiables. Voici quelques exemples : l’erreur WS \_ et les chaînes d’erreur, qui peuvent être stockées dans l’objet Error en fonction des informations reçues sur un canal non approuvé. L’utilisateur de l’objet d’erreur doit être prudent lors de l’inspection des informations de l’objet d’erreur et de la prise de décisions en fonction de ses valeurs.
-   Un utilisateur de l’objet d’erreur doit appeler [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) après avoir inspecté les informations relatives à l’erreur. Si ce n’est pas le cas, cela peut entraîner une accumulation de la mémoire.
-   Un utilisateur de l’objet d’erreur doit être très prudent lors de l' \_ utilisation \_ de la \_ valeur de divulgation d’erreur complète WS de l’énumération de la [**\_ \_ Divulgation**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) d’erreurs WS, car l’erreur générée peut contenir des informations privées qui ont été accumulées dans le cadre du processus d’enregistrement des erreurs.

 

 




