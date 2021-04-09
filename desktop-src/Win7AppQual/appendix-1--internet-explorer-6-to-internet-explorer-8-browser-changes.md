---
description: Le tableau suivant décrit les modifications apportées entre Microsoft Internet Explorer 6 et Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Modifications du navigateur IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865357"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Annexe 1 : modifications apportées à Internet Explorer 6 et au navigateur Internet Explorer 8

Le tableau suivant décrit les modifications apportées entre Microsoft Internet Explorer 6 et Windows Internet Explorer 8.



Modifications de la conception d’Internet Explorer 6 vers Internet Explorer 7

Modifications de conception d’Internet Explorer 7 vers Internet Explorer 8

$ {ROWSPAN2} $Internet Explorateur de versions $ {REMOVE} $  

Recherchez du code qui n’a pas été correctement détecté dans les cas d’Internet Explorer 6, Windows Internet Explorer 7 ou Internet Explorer 8 par le biais de la [détection de chaînes de l’agent utilisateur, des vecteurs de version ou des commentaires conditionnels](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Lorsqu’une chaîne d’agent utilisateur long rencontre un serveur qui accepte uniquement des chaînes UA plus courtes, les utilisateurs voient [une page d’erreur](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   L’affichage de compatibilité dans Internet Explorer 8, qui est activé par défaut pour les sites intranet, envoie une chaîne de l’agent utilisateur d’Internet Explorer 7. Pour faire la différence entre Internet Explorer 7 et l’affichage de compatibilité, recherchez le nouveau [jeton Trident](/archive/blogs/ie/).

Mises à jour de conformité de $ {ROWSPAN3} $ standards

-   S’applique aux [modes de document spécifiés](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   Le [mode d’affichage de compatibilité Internet Explorer 8](/archive/blogs/ie/), activé par défaut pour les sites intranet, [rétablit généralement les mises à jour de normes d’Internet Explorer 7 vers Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Utilisez l’en-tête http ou l’élément **meta** [EMULATEIE7 X-UA-Compatible](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) pour activer l’affichage de compatibilité sur des sites Web ou des pages Web spécifiques.

$ {REMOVE} $  

Exception en mode Quirks : vous n’avez pas besoin d’apporter des modifications de conformité aux normes pour les pages Web qui spécifient le mode Quirks DOCTYPE (en définissant le commutateur DOCTYPE « normes-conformité » sur « désactivé »).

S'applique aux normes d'Internet Explorer 7 ou au mode « strict » et plus :

-   Les [projournals XML](/previous-versions/windows/internet-explorer/ie-developer/) sur la première ligne du code source n’entraînent plus l’échec des déclarations DOCTYPE.
-   La zone de débordement de contenu du [modèle Box](/previous-versions/windows/internet-explorer/ie-developer/) et n’augmente plus automatiquement la taille de la zone div pour s’adapter au contenu.
-   [Certains filtres CSS](/previous-versions/windows/internet-explorer/ie-developer/) (par exemple, \* HTML, trait de \_ soulignement et/ \* \* /commentaire) ne sont pas pris en charge.
-   [Seul l’élément objet le plus à l’extérieur dans les objets imbriqués](/previous-versions/windows/internet-explorer/ie-developer/) est instancié.
-   Les [applications qui reposent sur l’élément Select](/previous-versions/windows/internet-explorer/ie-developer/) pour obtenir un HWND à utiliser avec les API Microsoft Win32 peuvent s’arrêter, car l' [élément Select](/archive/blogs/ie/) est désormais un contrôle sans fenêtre.
-   Le [format CDF (Channel Definition Format)](/previous-versions/aa740486(v=msdn.10)) n’est pas pris en charge, en faveur des flux RSS.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), format de création d’images conçu pour les systèmes X, n’est pas pris en charge.
-   Les [balises de base](/previous-versions/aa740486(v=msdn.10)) en dehors du document en-tête ne sont pas autorisées.

S'applique au mode standard d'Internet Explorer 8 et versions ultérieures :

-   Les [éléments P](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) non fermés sont fermés automatiquement lorsqu’ils sont suivis par des éléments [**table**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**Form**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**noframe**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)ou [**NoScript**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) .
-   Le [code HTML incorrect](/archive/blogs/ie/site-compatibility-and-ie8) n’est pas pris en charge, en faveur du balisage valide bien formé.
-   La syntaxe d' [attribut « ClassName »](/archive/blogs/ie/site-compatibility-and-ie8) n’est pas prise en charge, en faveur de la syntaxe « Class ».
-   [La collection d’attributs](/archive/blogs/ie/site-compatibility-and-ie8) ne contient pas tous les attributs possibles reconnus par Windows Internet Explorer.
-   L’ordre des attributs [a changé](/archive/blogs/ie/site-compatibility-and-ie8), ce qui affecte la collection d’attributs, InnerHtml et OuterHtml.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) respecte la casse et ne recherche pas les attributs de nom.
-   Les [sélecteurs de préfixe CSS génériques](/archive/blogs/ie/site-compatibility-and-ie8) (c’est-à-dire la \\ syntaxe v :) ne \* sont pas pris en charge, en faveur des noms de balises explicites.
-   Les [expressions CSS](/archive/blogs/ie/site-compatibility-and-ie8) ne sont pas prises en charge, en faveur d’une prise en charge CSS améliorée ou d’une logique DHTML.
-   Le code destiné aux méthodes d’objet JSON personnalisées peut être en conflit avec le [nouvel objet JSON natif](/archive/blogs/ie/site-compatibility-and-ie8) dans Internet Explorer 8.
-   Les [propriétés initiales non définies](/archive/blogs/ie/site-compatibility-and-ie8) sur l’objet currentStyle retournent retournent leur valeur initiale.
-   Les [valeurs de propriétés non spécifiées](/archive/blogs/ie/site-compatibility-and-ie8) sur l’objet de style objet currentStyle retournent retournent une chaîne vide (par exemple, consultez le [menu ASP.net et](/archive/blogs/giorgio/) le billet de blog sur les problèmes d’affichage IE8).

<!-- -->

-   Pour les sites et les applications où l’accessibilité est un problème, mettez à jour la [syntaxe Aria à travers tous les modes de rendu d’Internet Explorer](/archive/blogs/ie/).
-   Consultez la [liste complète des mises à jour CSS d’Internet Explorer 6 vers Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Améliorations de sécurité

-   Appliquer quel que soit le mode de document.
-   Vous pouvez désactiver les fonctionnalités de sécurité à l’aide de [stratégie de groupe](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   Le contournement de [Window. opener](/previous-versions/aa740486(v=msdn.10)) à l’invite window. Close n’est pas autorisé.
-   [La protection de la mise en cache d’objets](/previous-versions/windows/internet-explorer/ie-developer/) est activée par défaut, ce qui bloque l’accès aux références d’objets quand les utilisateurs accèdent à un nouveau domaine (s’applique à Internet Explorer 6 et versions ultérieures sur Windows XP avec Service Pack 2 (SP2) et versions ultérieures).
-   Les [scriptlets DHTML](/previous-versions/windows/internet-explorer/ie-developer/) sont désactivés par défaut.
-   [Les scripts qui écrivent dans la barre d’État](/previous-versions/windows/internet-explorer/ie-developer/) sont bloqués.
-   La [création d’URL peut échouer](/previous-versions/windows/internet-explorer/ie-developer/) si les URL ne respectent pas les instructions RFC.
-   Les [pages https affichent une page d’erreur](/previous-versions/windows/internet-explorer/ie-developer/) si le site est configuré sur SSLv2 uniquement, ou si le certificat de sécurité du site est obsolète ou non valide, contient des erreurs ou un chiffrement faible.
-   Seuls les [noms de domaine internationaux codés « Punycode »](/previous-versions/windows/internet-explorer/ie-developer/) sont pris en charge. D’autres formats tels que ANSI et UTF-8 sont bloqués.
-   Les [URL de script inter-domaines](/previous-versions/windows/internet-explorer/ie-developer/), la navigation redirigée dans les objets DOM et les navigations de frame sont bloquées.
-   Les [boîtes de dialogue modales ou non modales](/previous-versions/aa740486(v=msdn.10)) créées à partir du script peuvent sembler [légèrement plus volumineuses](/archive/blogs/ie/).
-   Affichage des [protocoles non sécurisés](/previous-versions/aa740486(v=msdn.10)) -source, Gopher (au niveau de WinInet) et Telnet ne fonctionnent pas.

<!-- -->

-   Le [filtre XSS](/archive/blogs/ie/) est activé par défaut, ce qui bloque les modèles de script qui ressemblent le plus souvent à des attaques XSS de type 1, sauf si vous les désactivez via un en-tête HTTP X-XSS-protection.
-   Les attaques de communication entre les documents inter-domaines comme le [script src](/archive/blogs/jscript/) ne sont pas prises en charge, en faveur des [fonctionnalités AJAX xdm et XDR](/archive/blogs/ie/)plus sûres.
-   Les sites compatibles AJAX qui [manipulent manuellement le hachage de l’URL](/previous-versions//cc891506(v=vs.85)) peuvent être interrompus par la nouvelle propriété de navigation Window. Location. Hash.
-   Les [nouvelles fonctionnalités AJAX](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) comme [xdm](/archive/blogs/ie/) ont des [**Propriétés natives**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) qui peuvent entrer en conflit avec des propriétés personnalisées existantes.
-   Le [contrôle de téléchargement de fichier](/archive/blogs/ie/) envoie uniquement le chemin d’accès du fichier, et non le chemin d’accès complet au serveur.
-   L’exécution du code HTML ou du script fourni avec un [ \* type MIME « image/ »](/archive/blogs/ie/) est bloquée.
-   La navigation dans un [cadre de niveau supérieur](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) vers un site dans un contexte de sécurité différent ouvre une nouvelle fenêtre ou un nouvel onglet au lieu de naviguer dans le frame existant.
-   Le [script encodé UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) est forcé dans l’encodage Windows-1252, ce qui peut provoquer un rendu de texte brut.
-   Les [pages http/https « mode mixte »](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) affichent une boîte de dialogue qui affiche par défaut les éléments sécurisés uniquement (par opposition à la valeur par défaut non sécurisée précédente). Les utilisateurs peuvent [choisir par erreur de bloquer les éléments http](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0), comme les images clés.
-   [DEP/NX est activé par défaut](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx), ce qui bloque certains modules complémentaires (c’est-à-dire les contrôles ActiveX et les objets com) qui sont générés à l’aide de versions antérieures d’ATL pour exécuter du code marqué comme « non exécutable » en mémoire.
-   [Le contenu renvoyé par un proxy Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) est bloqué si aucun tunnel SSL n’est établi en réponse à une demande de connexion au serveur d’origine.

Modifications architecturales

-   Appliquez quel que soit le mode de compatibilité ou le document.

<!-- -->

-   Le [mode protégé](/previous-versions/windows/internet-explorer/ie-developer/) est activé par défaut pour les [zones Internet, intranet et sites sensibles](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Ce mode [bloque les extensions de navigateur qui peuvent poser un risque de sécurité](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) à partir de l’exécution et des [applications à privilèges faibles de l’accès à des processus de privilège plus élevés](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), tels que le menu Démarrer, le panneau de configuration et le Registre Microsoft Windows (s’applique à Internet Explorer 7 et versions ultérieures sur Windows Vista et versions ultérieures).

<!-- -->

-   [Mise à jour du mode protégé](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): l’intranet s’exécute par défaut au niveau d’intégrité moyen (au lieu d’être faible).
-   [Internet Explorer faiblement couplé](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) peut bloquer des modules complémentaires (c’est-à-dire des contrôles ActiveX et des objets com) qui effectuent l’une des opérations suivantes :
    -   Utilisez les techniques de hiérarchie Windows pour localiser les fenêtres Frame et onglet de l’interface utilisateur (qui s’exécutent désormais dans des processus distincts à des niveaux d’intégrité différents).
    -   Créez une sous-classe du frame de l’interface utilisateur (maintenant au niveau d’intégrité moyenne) à partir d’un processus d’onglets de faible intégrité.
    -   Utilisez des techniques de messagerie non prises en charge entre les onglets et la trame de l’interface utilisateur.



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
