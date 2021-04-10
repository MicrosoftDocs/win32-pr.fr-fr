---
description: Les journaux des événements stockent des événements importants pour le compte du système et des applications qui s’exécutent sur le système.
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: Instructions de journalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115199"
---
# <a name="logging-guidelines"></a>Instructions de journalisation

Les journaux des événements stockent des événements importants pour le compte du système et des applications qui s’exécutent sur le système. Étant donné que les fonctions de journalisation sont à usage général, vous devez déterminer quelles informations sont appropriées au journal. En règle générale, vous devez enregistrer uniquement les informations qui peuvent être utiles pour diagnostiquer un problème matériel ou logiciel. La journalisation des événements n’est pas destinée à être utilisée en tant qu’outil de suivi.

## <a name="choosing-events-to-log"></a>Choix des événements à consigner

Voici des exemples de cas dans lesquels la journalisation des événements peut être utile :

-   Problèmes de ressources. La journalisation d’un événement d’avertissement lorsque l’allocation de mémoire échoue peut aider à indiquer la cause d’une situation de mémoire insuffisante.
-   Problèmes matériels. Si un pilote de périphérique rencontre un délai d’attente de contrôleur de disque, une panne d’alimentation dans un port parallèle ou une erreur de données à partir d’un réseau ou d’une carte série, le pilote de périphérique peut consigner des informations sur ces événements pour aider l’administrateur système à diagnostiquer des problèmes matériels.
-   Secteurs incorrects. Si un pilote de disque rencontre un secteur défectueux, il peut être en mesure de lire ou d’écrire dans le secteur après une nouvelle tentative de l’opération, mais le secteur sera incorrect. Si le pilote de disque peut continuer, il doit consigner un événement d’avertissement ; dans le cas contraire, il doit consigner un événement d’erreur. Si un pilote de système de fichiers trouve un grand nombre de secteurs incorrects et les corrige, la journalisation des événements d’avertissement peut aider un administrateur à déterminer que le disque peut être en panne.
-   Événements d’informations. Une application serveur (par exemple, un serveur de base de données) enregistre une ouverture de session utilisateur, l’ouverture d’une base de données ou le démarrage d’un transfert de fichiers. Le serveur peut également consigner d’autres événements tels que des erreurs (impossible d’accéder à un fichier, un processus hôte déconnecté, etc.), une base de données endommagée ou si un transfert de fichiers a réussi.

## <a name="writing-messages"></a>Écriture de messages

Les messages doivent être compréhensibles pour les administrateurs et les utilisateurs qui tentent de résoudre un problème. Un message doit contenir toutes les informations nécessaires pour comprendre ce qui a provoqué le problème et comment le corriger.

Évitez d’écrire un message énigmatique tel que «un paquet de pilote reçu à partir du sous-système d’e/s n’était pas valide. Les données sont le paquet». Un message meilleur indique que le pilote en question fonctionne correctement, mais qu’il enregistre des paquets au format incorrect. Il est possible d’indiquer qu’une version Unicode du pilote est nécessaire pour corriger le problème. Pour plus d’informations sur l’écriture de bons messages d’erreur, consultez [instructions relatives aux messages d’erreur](/windows/desktop/Debug/error-message-guidelines).

N’utilisez pas de tabulations ou de virgules dans le texte du message, car les journaux des événements peuvent être enregistrés en tant que fichiers texte séparés par des virgules ou des tabulations. De nombreuses organisations importent ces fichiers dans des bases de données, et les caractères de mise en forme supplémentaires nécessitent une manipulation manuelle.

Lorsque vous utilisez des noms UNC ou d’autres liens qui contiennent des espaces, placez le nom entre crochets pointus. Par exemple, <\\ \\ *Nom_Partage* \\ *ServerName*>. Vous pouvez écrire une URL à la fin du message qui dirige l’utilisateur vers le document d’aide associé. L’URL doit être un nom d’hôte DNS complet. Par exemple, vous pouvez ajouter le texte suivant à vos messages : « pour plus d’informations sur ce message, consultez notre site de support technique à l’adresse https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp . » Le lien mène à une page ASP qui redirige l’utilisateur vers le contenu relatif au message d’erreur. Il analyse les paramètres supplémentaires (transmis lorsque l’utilisateur clique sur l’URL) pour déterminer où rediriger l’utilisateur.

Les arguments passés à la fonction [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) sont ajoutés à l’URL comme suit :

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

Si le nom de la société, le nom du produit, la version du produit, le nom du fichier et la version du fichier de l’en-tête de la DLL de message pour la source de l’événement sont valides, ils sont également ajoutés à l’URL :

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>Réduction de la surcharge

L’enregistrement des événements consomme des ressources telles que l’espace disque et le temps processeur. La quantité d’espace disque nécessaire pour un journal des événements et la surcharge d’une application qui journalise les événements dépend de la quantité d’informations que vous choisissez de consigner. C’est pourquoi il est important de ne journaliser que les informations essentielles. Il est également conseillé de placer les appels de journalisation des événements dans un chemin d’erreur dans le code plutôt que dans le chemin de code principal, ce qui réduit les performances.

La quantité d’espace disque requise pour chaque enregistrement de journal des événements comprend les membres de la structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Il s’agit d’une structure de longueur variable. les chaînes et les données binaires sont stockées à la suite de la structure.

 

 
