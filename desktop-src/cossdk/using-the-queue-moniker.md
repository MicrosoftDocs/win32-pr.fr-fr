---
description: Le moniker de la file d’attente est utilisé pour activer un composant mis en file d’attente par programmation.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Utilisation du moniker de la file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938b4c0c8afc19e953d7f62f17f95bbd63f387e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473685"
---
# <a name="using-the-queue-moniker"></a>Utilisation du moniker de la file d’attente

Le moniker de la file d’attente est utilisé pour activer un composant mis en file d’attente par programmation. Le moniker de la file d’attente requiert qu’il reçoive l’ID de classe (CLSID) de l’objet à appeler à partir du nouveau moniker directement à sa droite. Lorsqu’il est préfixé à gauche, le nouveau moniker passe le CLSID au moniker à gauche de celui-ci.

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

Le paramètre de nom complet GetObject est « queue:/New : », suivi de l’ID de programme ou du GUID de forme chaîne, avec ou sans accolades, de l’objet serveur à instancier. Les exemples suivants illustrent trois activations valides d’un composant avec le moniker de file d’attente :

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

Le paramètre [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) Display Name est « queue:/New : », suivi de l’ID de programme ou du GUID de forme chaîne, avec ou sans accolades, de l’objet serveur à instancier. Les exemples suivants illustrent trois activations valides d’un composant avec le moniker de file d’attente :

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a>Remarques

Le moniker de la file d’attente accepte des paramètres facultatifs qui modifient les propriétés du message envoyé à Message Queuing. Par exemple, pour faire en sorte que le message Message Queuing soit envoyé avec une priorité 6, le composant mis en file d’attente est activé comme suit :

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

Le tableau suivant répertorie les paramètres du moniker de la file d’attente qui affectent la file d’attente de destination.




| Paramètre | Description | 
|-----------|-------------|
| <em>ComputerName</em><br /> | Spécifie la partie nom d’ordinateur d’un nom de chemin d’accès de file d’attente Message Queuing. Le nom du chemin d’accès de la file d’attente Message Queuing est au format <em>ComputerName</em> \<em> QueueName </em> . S’il n’est pas spécifié, le nom de l’ordinateur associé à l’application configurée est utilisé.<br /> | 
| <em>QueueName</em><br /> | Spécifie le nom de la file d’attente Message Queuing. Le nom du chemin d’accès de la file d’attente Message Queuing est au format <em>ComputerName</em> \<em> QueueName </em> . S’il n’est pas spécifié, le nom de la file d’attente associé à l’application configurée est utilisé.<br /> Pour obtenir une file d’attente non transactionnelle, vous pouvez d’abord spécifier le nom de la file d’attente, puis créer une application COM+ portant le même nom.<br /> | 
| <em>PathName</em><br /> | Spécifie le nom complet du chemin d’accès de la file d’attente Message Queuing. S’il n’est pas spécifié, le nom du chemin d’accès de la file d’attente Message Queuing associé à l’application configurée est utilisé. Pour remplacer le nom de destination, le chemin d’accès peut être spécifié sous la forme suivante pour une installation de Message Queuing groupe de travail :<br /> Queue :<em>pathname</em> = <em>nomordinateur</em>\private $ \ AppName/New : MyProject. CMyClass<br /><blockquote>[!Note]<br />les langages de programmation C et Microsoft Visual C++ requièrent deux barres obliques inverses pour représenter une barre oblique inverse dans les littéraux de chaîne, par exemple, chicago \\ payroll.</blockquote><br /> | 
| <em>FormatName</em><br /> | Lorsque vous marquez une application COM+ comme en file d’attente, COM+ crée une file d’attente Message Queuing dont le nom est identique à celui de l’application. Le nom de format Message Queuing de cette file d’attente se trouve dans le catalogue COM+, associé à l’application COM+. Pour remplacer le nom de destination, le nom de format peut être spécifié sous la forme suivante pour une installation Message Queuing groupe de travail :<br /> Queue :<em>FormatName</em>= direct = OS :<em>nom_ordinateur</em>\private $ \ AppName/New : ProgID<br /> Dans une configuration Active Directory, « PRIVATE $ » n’est pas spécifié dans le nom de la file d’attente. <br /> | 




 

> [!Note]  
> Les paramètres facultatifs du moniker de la file d’attente sont traités de gauche à droite. Spécifiez chaque mot clé une seule fois. La spécification du paramètre *pathname* remplace les paramètres *ComputerName* et *QueueName*. Un paramètre *FormatName* spécifique supprime la connaissance préalable d’un paramètre *ComputerName*, *QueueName* et *pathname* .

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Association de l’écouteur de composants en file d’attente à une file d’attente privée spécifique

L’écouteur de composants en file d’attente COM+ reçoit uniquement des files d’attente associées à l’application COM+ marquée en file d’attente. Lorsque vous marquez une application COM+ comme en file d’attente, COM+ crée une file d’attente Message Queuing dont le nom est identique à celui de l’application. Le nom de format Message Queuing de cette file d’attente se trouve dans le catalogue COM+, associé à l’application COM+. Lorsque l’application COM+ est démarrée et marquée comme Listen, un écouteur dans le processus de l’application COM+ est démarré et la file d’attente est ouverte. Le tableau suivant répertorie les paramètres du moniker de la file d’attente qui affectent le message de Message Queuing.




| Paramètre | Description | 
|-----------|-------------|
| <em>AppSpecific</em><br /> | Spécifie un entier non signé, par exemple, AppSpecific = 12345.<br /> | 
| <em>AuthLevel</em><br /> | Spécifie le niveau d’authentification du message. Un message authentifié est signé numériquement et requiert un certificat pour l’utilisateur qui envoie le message. Valeurs acceptables :<br /><ul><li>MQMSG_AUTH_LEVEL_NONE, 0</li><li>MQMSG_AUTH_LEVEL_ALWAYS, 1</li></ul> | 
| <em>Distribution</em><br /> | Spécifie l’option de remise de message. Cette valeur est ignorée pour les files d’attente transactionnelles. Valeurs acceptables :<br /><ul><li>MQMSG_DELIVERY_EXPRESS, 0</li><li>MQMSG_DELIVERY_RECOVERABLE, 1</li></ul> | 
| <em>EncryptAlgorithm</em><br /> | Spécifie l’algorithme de chiffrement à utiliser par Message Queuing pour chiffrer et déchiffrer le message. Valeurs acceptables :<br /><ul><li>CALG_RC2, CALG_RC4</li><li>Toute valeur entière acceptable pour Message Queuing pour un <em>EncryptAlgorithm</em>.</li></ul> | 
| <em>HashAlgorithm</em><br /> | Spécifie une fonction de hachage de chiffrement. Valeurs acceptables :<br /><ul><li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li><li>Toute valeur entière acceptable pour Message Queuing pour un <em>HashAlgorithm</em>.</li></ul> | 
| Journal<br /> | Spécifie l’option Message Queuing le journal des messages. Valeurs acceptables :<br /><ul><li>MQMSG_JOURNAL_NONE, 0</li><li>MQMSG_DEADLETTER, 1</li><li>MQMSG_JOURNAL, 2</li></ul> | 
| <em>Étiquette</em><br /> | Spécifie une chaîne d’étiquette de message jusqu’à MQ_MAX_MSG_LABEL_LEN caractères. <br /> | 
| <em>MaxTimeToReachQueue</em><br /> | Spécifie la durée maximale, en secondes, pendant laquelle le message atteint la file d’attente. <br /> Valeurs acceptables :<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Nombre de secondes</li></ul> | 
| <em>MaxTimeToReceive</em><br /> | Spécifie la durée maximale, en secondes, pendant laquelle le message est reçu par l’application cible. Valeurs acceptables :<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Nombre de secondes</li></ul> | 
| <em>Priorité</em><br /> | Spécifie un niveau de priorité de message dans les valeurs Message Queuing autorisées.<br /> Valeurs acceptables :<br /><ul><li>MQ_MIN_PRIORITY, 0</li><li>MQ_MAX_PRIORITY, 7</li><li>MQ_DEFAULT_PRIORITY, 3</li><li>Nombre compris entre 0 et 7</li></ul> | 
| <em>PrivLevel</em><br /> | Spécifie un niveau de confidentialité, utilisé pour chiffrer les messages.<br /> Valeurs acceptables :<br /><ul><li>MQMSG_PRIV_LEVEL_NONE, AUCUN, 0</li><li>MQMSG_PRIV_LEVEL_BODY, CORPS,</li><li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li><li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li></ul> | 
| <em>Trace</em><br /> | Spécifie les options de trace utilisées dans le suivi Message Queuing routage.<br /> Valeurs acceptables :<br /><ul><li>MQMSG_TRACE_NONE, 0</li><li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</li></ul> | 




 

L’ensemble complet des fonctions du kit de développement logiciel (SDK) d’administration COM+ est disponible à l’aide d’objets COM. Cela permet à n’importe quel programme de démarrer et d’arrêter les applications COM+ selon les besoins.

> [!Note]  
> Lors du démarrage d’une application COM+, il s’agit de l’application en cours d’exécution, et non des composants individuels de l’application. Si une application appelle un composant non mis en file d’attente, l’application COM+ qui contient le composant est démarrée. Si la case à cocher écouteur est activée, l’écouteur démarre et commence le traitement des messages pour les composants en file d’attente. Alors que le service de composants en file d’attente peut être démarré de cette manière, si vous empaquetez des composants mis en file d’attente et non mis en file d’attente dans une seule application COM+, assurez-vous que vous souhaitez vraiment que les composants en file d’attente démarrent si un composant non mis en file d’attente est exécuté. Si ce n’est pas le cas, empaquetez les composants mis en file d’attente dans une application COM+ distincte des autres composants.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation des files d’attente de composants](activating-component-queues.md)
</dt> </dl>

 

 




