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
# <a name="accessing-services-using-java"></a><span data-ttu-id="9ad9c-103">Accès aux services à l’aide de Java</span><span class="sxs-lookup"><span data-stu-id="9ad9c-103">Accessing Services Using Java</span></span>

<span data-ttu-id="9ad9c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ad9c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9ad9c-105">Vous pouvez également accéder aux services Microsoft Agent à partir d’une applet Java.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="9ad9c-106">La plupart des fonctions accessibles par le biais des interfaces de l’agent Microsoft retournent des valeurs par le biais de paramètres passés par référence.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="9ad9c-107">Pour passer ces paramètres à partir de Java, il est nécessaire de créer des tableaux à un seul élément dans votre code et de les passer en tant que paramètres à la fonction appropriée.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="9ad9c-108">Si vous utilisez Microsoft Visual J++ et que vous avez exécuté l’Assistant bibliothèque de types Java sur le serveur Microsoft Agent, reportez-vous au fichier summary.txt pour examiner les fonctions qui requièrent des arguments de tableau.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="9ad9c-109">La procédure est similaire à celle de C ; vous utilisez l’interface [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) pour créer une instance du serveur, puis charger le caractère :</span><span class="sxs-lookup"><span data-stu-id="9ad9c-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


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



<span data-ttu-id="9ad9c-110">La procédure est légèrement différente lors du chargement de caractères à partir d’un emplacement distant HTTP, tel qu’un site Web.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="9ad9c-111">Dans ce cas, la méthode [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) est asynchrone et lève une exception com de E \_ en attente (0x8000000a).</span><span class="sxs-lookup"><span data-stu-id="9ad9c-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="9ad9c-112">Vous devez intercepter cette exception et la gérer correctement comme le fait les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ad9c-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


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



<span data-ttu-id="9ad9c-113">Ensuite, accédez à l’interface [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) qui vous permet d’accéder à ses méthodes :</span><span class="sxs-lookup"><span data-stu-id="9ad9c-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="9ad9c-114">De même, pour être averti des événements, vous devez implémenter l’interface [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) ou [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , en créant et en inscrivant un objet de ce type :</span><span class="sxs-lookup"><span data-stu-id="9ad9c-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


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



<span data-ttu-id="9ad9c-115">Pour pouvoir accéder à Microsoft Agent à partir d’une applet Java, vous devez générer des classes Java que vous installez avec l’applet.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="9ad9c-116">Vous pouvez utiliser l’Assistant bibliothèque de types Java Visual J++, par exemple, pour générer ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="9ad9c-117">Si vous envisagez d’héberger l’applet sur une page Web, vous devez créer un fichier CAB Java signé contenant les fichiers de classe générés qui sont téléchargés avec la page.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="9ad9c-118">Les fichiers de classe sont nécessaires pour accéder au serveur Microsoft Agent, car il s’agit d’un objet COM, qui s’exécute en dehors du sandbox Java.</span><span class="sxs-lookup"><span data-stu-id="9ad9c-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="9ad9c-119">Pour en savoir plus sur la sécurité de Trust-Based pour Java, consultez <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="9ad9c-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 