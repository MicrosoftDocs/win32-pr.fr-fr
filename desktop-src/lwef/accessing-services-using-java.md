---
title: Accès aux services à l’aide de Java
description: Accès aux services à l’aide de Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940897"
---
# <a name="accessing-services-using-java"></a>Accès aux services à l’aide de Java

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Vous pouvez également accéder aux services Microsoft Agent à partir d’une applet Java. La plupart des fonctions accessibles par le biais des interfaces de l’agent Microsoft retournent des valeurs par le biais de paramètres passés par référence. Pour passer ces paramètres à partir de Java, il est nécessaire de créer des tableaux à un seul élément dans votre code et de les passer en tant que paramètres à la fonction appropriée. Si vous utilisez Microsoft Visual J++ et que vous avez exécuté l’Assistant bibliothèque de types Java sur le serveur Microsoft Agent, reportez-vous au fichier summary.txt pour examiner les fonctions qui requièrent des arguments de tableau. La procédure est similaire à celle de C ; vous utilisez l’interface [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) pour créer une instance du serveur, puis charger le caractère :


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



La procédure est légèrement différente lors du chargement de caractères à partir d’un emplacement distant HTTP, tel qu’un site Web. Dans ce cas, la méthode [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) est asynchrone et lève une exception com de E \_ en attente (0x8000000a). Vous devez intercepter cette exception et la gérer correctement comme le fait les fonctions suivantes :


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



Ensuite, accédez à l’interface [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) qui vous permet d’accéder à ses méthodes :


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



De même, pour être averti des événements, vous devez implémenter l’interface [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) ou [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , en créant et en inscrivant un objet de ce type :


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



Pour pouvoir accéder à Microsoft Agent à partir d’une applet Java, vous devez générer des classes Java que vous installez avec l’applet. Vous pouvez utiliser l’Assistant bibliothèque de types Java Visual J++, par exemple, pour générer ces fichiers. Si vous envisagez d’héberger l’applet sur une page Web, vous devez créer un fichier CAB Java signé contenant les fichiers de classe générés qui sont téléchargés avec la page. Les fichiers de classe sont nécessaires pour accéder au serveur Microsoft Agent, car il s’agit d’un objet COM, qui s’exécute en dehors du sandbox Java. Pour en savoir plus sur la sécurité de Trust-Based pour Java, consultez <https://www.microsoft.com/java/security> .

 

 