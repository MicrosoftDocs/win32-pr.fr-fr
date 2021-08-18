---
description: cette rubrique fournit un exemple d’écriture d’un script qui obtient des données via Microsoft Windows HTTP Services (WinHTTP) de façon synchrone ou asynchrone.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Récupération de données à l’aide d’un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e018aa680808feddc021c7c03937d085b0d0f787c3213720cbb5e94a46a85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133062"
---
# <a name="retrieving-data-using-script"></a>Récupération de données à l’aide d’un script

cette rubrique fournit un exemple d’écriture d’un script qui obtient des données via Microsoft Windows HTTP Services (WinHTTP) de façon synchrone ou asynchrone. Les concepts présentés dans cet exemple fournissent la base de l’écriture d’applications clientes ou de serveur de couche intermédiaire qui requièrent l’accès aux données à l’aide du protocole HTTP.

-   [Conditions préalables et configuration requise](#prerequisites-and-requirements)
-   [Récupération de données de façon synchrone](#retrieving-data-synchronously)
-   [Récupération de données de façon asynchrone](#retrieving-data-asynchronously)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites-and-requirements"></a>Conditions préalables et configuration requise

outre les connaissances pratiques de Microsoft JScript, cet exemple nécessite les éléments suivants :

-   version actuelle du kit de développement logiciel (SDK) Microsoft Windows.
-   l’outil de configuration de proxy pour établir les paramètres de proxy pour les Services HTTP Microsoft Windows (WinHTTP), si votre connexion à Internet s’effectue via un serveur proxy. Pour plus d’informations, consultez [ProxyCfg.exe, un outil de configuration de proxy](proxycfg-exe--a-proxy-configuration-tool.md).
-   Une bonne connaissance de la terminologie et des concepts relatifs au [réseau](network-terminology.md) .

## <a name="retrieving-data-synchronously"></a>Récupération de données de façon synchrone

**Pour créer un script qui obtient le texte d’une page Web de façon synchrone, procédez comme suit :**

1.  Ouvrez un éditeur de texte.
2.  Copiez le code suivant dans l’éditeur de texte.

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  Enregistrez le fichier en tant que « Retrieve.js ».
4.  À partir d’une invite de commandes, tapez « cscript Retrieve.js » et appuyez sur entrée.

Vous avez maintenant un script qui utilise un objet [**WinHttpRequest**](winhttprequest.md) pour obtenir le code source HTML de la page Web à l’adresse https://www.microsoft.com . Vous devrez peut-être attendre quelques secondes avant que le code n’apparaisse.

L’application contient une seule fonction, « getText ». La première ligne du script crée l’objet [**WinHttpRequest**](winhttprequest.md) .


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



lorsque le moteur de JScript rencontre cette ligne, il crée une instance de cet objet. si vous recevez le message d’erreur « ActiveX composant ne peut pas créer d’objet », sur cette ligne, le WinHttp.dll n’a probablement pas été correctement inscrit ou n’est pas présent sur le système.

La ligne suivante du script appelle la méthode [**Open**](iwinhttprequest-open.md) .


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Trois paramètres spécifient le [*verbe http*](glossary.md) à utiliser, le nom de la ressource et s’il faut utiliser WinHTTP de façon synchrone ou asynchrone. Dans cet exemple, la méthode utilise le *verbe http*« obtenir » pour obtenir des données à partir de https://www.microsoft.com . La spécification de la **valeur false** pour le dernier paramètre détermine que la transaction se produit de façon synchrone. La méthode [**Open**](iwinhttprequest-open.md) n’établit pas de connexion à la ressource, car le nom peut le supposer. Au lieu de cela, il initialise les structures de données internes qui maintiennent les informations sur la session, la connexion et la demande.

La méthode [**Send**](iwinhttprequest-send.md) assemble les en-têtes de requête et envoie la demande. En cas d’appel en mode synchrone, la méthode [**Send**](iwinhttprequest-send.md) attend également une réponse avant d’autoriser l’application à continuer.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Après l’envoi de la demande, le script retourne la valeur de la propriété [**responseText**](iwinhttprequest-responsetext.md) de l’objet [**WinHttpRequest**](winhttprequest.md) . Cette propriété contient le corps d’entité de la réponse, dans ce cas, la source d’un document.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



L’exécution du script s’interrompt pendant que l’intégralité du texte de la ressource est récupérée. Le texte de la ressource est retourné à partir de la fonction et affiché.

L’objet [**WinHttpRequest**](winhttprequest.md) garantit que toutes les ressources internes qui sont allouées pour la transaction http sont libérées.

## <a name="retrieving-data-asynchronously"></a>Récupération de données de façon asynchrone

La récupération de données de façon asynchrone à l’aide de WinHTTP est très similaire à la récupération de données de façon synchrone. Modifiez le script de la section précédente en effectuant deux petites modifications.

1.  Définissez le troisième paramètre de la méthode [**Open**](iwinhttprequest-open.md) sur « true » au lieu de « false » pour spécifier que les méthodes WinHTTP doivent être exécutées de façon asynchrone.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Appelez la méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) avant d’accéder à la propriété [**responseText**](iwinhttprequest-responsetext.md) pour vous assurer que l’intégralité de la réponse a été reçue.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

Le principal avantage de l’utilisation de WinHTTP de manière asynchrone dans le script est que la méthode [**Send**](iwinhttprequest-send.md) est retournée immédiatement. La requête est préparée et envoyée par un thread de travail. Cela permet à votre application d’effectuer d’autres tâches pendant qu’elle attend la réponse. Avant de tenter d’accéder à la réponse, assurez-vous que l’intégralité de la réponse a été reçue en appelant la méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) . Sinon, une erreur peut se produire.

La méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) peut également être utilisée pour spécifier une valeur de délai d’attente pour la transaction. Un paramètre facultatif vous permet de spécifier la valeur du délai d’attente en secondes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Demande de commentaires HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



