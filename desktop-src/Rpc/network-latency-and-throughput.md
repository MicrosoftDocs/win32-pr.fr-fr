---
title: Latence et débit du réseau
description: Latence du réseau et débit avec appel de procédure distante (RPC).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197261"
---
# <a name="network-latency-and-throughput"></a>Latence et débit du réseau

Trois problèmes majeurs se rapportent à une utilisation optimale du réseau :

-   Latence du réseau
-   Saturation du réseau
-   Implications en matière de traitement des paquets

Cette section présente une tâche de programmation nécessitant l’utilisation d’un RPC, puis conçoit deux solutions : une mauvaise écriture et une bonne écriture. Les deux solutions sont ensuite examinées et leur impact sur les performances du réseau est abordé.

Avant de discuter des deux solutions, les sections suivantes décrivent et clarifient les problèmes de performances liés au réseau.

## <a name="network-latency"></a>Latence du réseau

La bande passante réseau et la latence du réseau sont des termes distincts. Les réseaux à bande passante élevée ne garantissent pas une faible latence. Par exemple, un chemin d’accès réseau qui traverse une liaison satellite a souvent une latence élevée, même si le débit est très élevé. Il n’est pas rare qu’une boucle de réseau traverse un lien satellite pour avoir cinq secondes ou plus de latence. L’implication d’un tel délai est la suivante : une application conçue pour envoyer une demande, attendre une réponse, envoyer une autre demande, attendre une autre réponse, etc., attendra au moins cinq secondes pour chaque échange de paquets, quelle que soit la vitesse du serveur. Malgré la rapidité accrue des ordinateurs, les transmissions par satellite et les supports réseau sont basés sur la vitesse de la lumière, qui reste généralement constante. Par conséquent, il est peu probable que des améliorations de la latence des réseaux satellites existants se produisent.

## <a name="network-saturation"></a>Saturation du réseau

Une certaine saturation se produit dans de nombreux réseaux. Les réseaux les plus faciles à saturer sont des liens de modem lents, tels que des modems analogiques 56k standard. Toutefois, les liaisons Ethernet avec de nombreux ordinateurs sur un seul segment peuvent également être saturées. Il en va de même pour les réseaux étendus avec une faible bande passante ou un lien surchargé, tel qu’un routeur ou un commutateur qui peut gérer une quantité limitée de trafic. Dans ce cas, si le réseau envoie plus de paquets que son lien le plus faible peut gérer, il supprime des paquets. Pour éviter toute congestion, la pile TCP Windows revient en arrière lorsque des paquets supprimés sont détectés, ce qui peut entraîner des retards importants.

## <a name="packet-processing-implications"></a>Implications en matière de traitement des paquets

Lorsque des programmes sont développés pour des environnements de niveau supérieur tels que RPC, COM et même Windows Sockets, les développeurs ont tendance à oublier la quantité de travail qui se produit en arrière-plan pour chaque paquet envoyé ou reçu. Lorsqu’un paquet arrive à partir du réseau, une interruption de la carte réseau est servie par l’ordinateur. Un appel de procédure différé (DPC) est alors mis en file d’attente et doit être effectué via les pilotes. Si une forme de sécurité est utilisée, il peut être nécessaire de déchiffrer le paquet ou le hachage de chiffrement vérifié. Un certain nombre de contrôles de validité doivent également être effectués à chaque État. Le paquet arrive uniquement à la destination finale : le code du serveur. L’envoi de plusieurs petits segments de données entraîne une surcharge de traitement des paquets pour chaque petit segment de données. L’envoi d’un grand segment de données tend à consommer beaucoup moins de temps processeur dans le système, même si le coût d’exécution de nombreux petits fragments par rapport à un grand segment peut être le même pour l’application serveur.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Exemple 1 : serveur RPC mal conçu

Imaginez une application qui doit accéder à des fichiers distants, et la tâche en cours consiste à concevoir une interface RPC pour manipuler le fichier distant. La solution la plus simple consiste à mettre en miroir les routines de fichier Studio pour les fichiers locaux. Cela peut entraîner un nettoyage et une interface familière trompeur. Voici un fichier. idl abrégé :

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

Cela semble assez élégant, mais en fait, il s’agit d’une recette à temps pour les sinistres de performances. Contrairement à l’opinion populaire, l’appel de procédure distante n’est pas simplement un appel de procédure locale avec un câble entre l’appelant et l’appelé.

Pour voir comment cette recette grave les performances, envisagez un fichier de 2K, où 20 octets sont lus depuis le début, puis 20 octets à partir de la fin, et voyez comment cela s’effectue. Côté client, les appels suivants sont effectués (de nombreux chemins de code sont omis par souci de concision) :

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Imaginez maintenant que le serveur est séparé du client par un lien satellite avec un temps d’aller-retour de cinq secondes. Chacun de ces appels doit attendre une réponse avant de pouvoir continuer, ce qui signifie un minimum absolu pour l’exécution de cette séquence de 25 secondes. En considérant que nous récupérons uniquement 40 octets, il s’agit d’un ralentissement des performances Outrageously. Les clients de cette application seraient furieux.

Imaginez maintenant que le réseau est saturé, car la capacité d’un routeur quelque part dans le chemin d’accès réseau est trop lourde. Cette conception force le routeur à gérer au moins 10 paquets si nous n’avons pas de sécurité (une pour chaque demande et une pour chaque réponse). Cela ne constitue pas une bonne chose.

Cette conception force également le serveur à recevoir cinq paquets et à envoyer cinq paquets. Là encore, l’implémentation n’est pas très bonne.

## <a name="example-2-a-better-designed-rpc-server"></a>Exemple 2 : serveur RPC mieux conçu

Nous allons modifier la conception de l’interface décrite dans l’exemple 1 et voir si nous pouvons la rendre plus efficace. Il est important de noter que le fait de rendre ce serveur vraiment correct nécessite une connaissance du modèle d’utilisation pour les fichiers donnés : cette connaissance n’est pas prise en compte pour cet exemple. Par conséquent, il s’agit d’un serveur RPC mieux conçu, mais pas d’un serveur RPC conçu de manière optimale.

L’idée de cet exemple est de réduire autant d’opérations distantes que possible en une seule opération. La première tentative est la suivante :

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

Dans cet exemple, toutes les opérations sont réduites en lecture et en écriture, ce qui permet un Open facultatif sur la même opération, ainsi qu’une fermeture et une recherche facultatives.

Cette même séquence d’opérations, lorsqu’elle est écrite sous une forme abrégée, ressemble à ceci :

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Lors de l’examen du serveur RPC le mieux conçu, le deuxième appel du serveur vérifie que le *\_ nom de fichier* est **null** et utilise le fichier ouvert stocké dans l’appel d’offres. Il voit ensuite les instructions de recherche et place le pointeur de fichier 20 octets avant la fin avant de lire. Une fois terminé, il reconnaît que l’indicateur **CloseWhenDone** est défini sur **true** et ferme le fichier, puis ferme l’appel d’offres.

Sur le réseau à latence élevée, cette version améliorée prend 10 secondes pour s’exécuter (2,5 fois plus vite) et nécessite le traitement de seulement quatre paquets. deux réceptions du serveur et deux envois à partir du serveur. Le *IFS* supplémentaire et le démarshaling du serveur sont négligeables par rapport à tout le reste.

Si le classement de causalité est correctement spécifié, l’interface peut même être rendue asynchrone et les deux appels peuvent être envoyés en parallèle. Lorsque le classement de causalité est utilisé, les appels sont toujours distribués dans l’ordre, ce qui signifie que sur le réseau à latence élevée, seul un délai de cinq secondes est écoulé, même si le nombre de paquets envoyés et reçus est le même.

Nous pouvons le réduire encore plus loin en créant une méthode qui prend un tableau de structures, chaque membre du tableau décrivant une opération de fichier particulière ; variation distante des e/s de ventilation/regroupement. L’approche s’acquitte du fait que le résultat de chaque opération ne nécessite pas de traitement supplémentaire sur le client ; en d’autres termes, l’application va lire les 20 octets à la fin, quel que soit le niveau de lecture des 20 premiers octets.

Toutefois, si un traitement doit être effectué sur les 20 premiers octets après les avoir lus pour déterminer l’opération suivante, la réduction de tout en une opération ne fonctionne pas (au moins dans tous les cas). L’élégance du RPC est qu’une application peut avoir les deux méthodes dans l’interface et appeler l’une ou l’autre des méthodes en fonction des besoins.

En général, lorsque le réseau est impliqué, il est préférable de combiner autant d’appels que possible dans un appel unique. Si une application a deux activités indépendantes, utilisez des opérations asynchrones et laissez-les s’exécuter en parallèle. Pour l’essentiel, gardez le pipeline complet.

 

 




