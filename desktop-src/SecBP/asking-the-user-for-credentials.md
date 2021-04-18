---
description: Il se peut que votre application doive inviter l’utilisateur à entrer les informations de nom d’utilisateur et de mot de passe pour éviter de stocker un mot de passe administrateur ou pour vérifier que le jeton détient les privilèges appropriés.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Demande d’informations d’identification à l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534038"
---
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="6f9ee-103">Demande d’informations d’identification à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6f9ee-103">Asking the User for Credentials</span></span>

<span data-ttu-id="6f9ee-104">Il se peut que votre application doive inviter l’utilisateur à entrer les informations de nom d’utilisateur et de mot de passe pour éviter de stocker un mot de passe administrateur ou pour vérifier que le jeton détient les privilèges appropriés.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="6f9ee-105">Toutefois, il suffit de demander des informations d’identification pour former les utilisateurs à les fournir à une boîte de dialogue aléatoire, non identifiée, qui s’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="6f9ee-106">La procédure suivante est recommandée pour réduire cet effet de formation.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="6f9ee-107">**Pour acquérir correctement les informations d’identification de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="6f9ee-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="6f9ee-108">Informez l’utilisateur, en utilisant un message qui fait clairement partie de votre application, qu’il verra une boîte de dialogue qui demande son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="6f9ee-109">Vous pouvez également utiliser la structure [**CREDUI \_ info**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) sur l’appel à [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) pour transmettre des données d’identification ou un message.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="6f9ee-110">Appelez [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="6f9ee-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="6f9ee-111">Notez que le nombre maximal de caractères spécifié pour les informations de nom d’utilisateur et de mot de passe comprend le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="6f9ee-112">Appelez [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) et [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) pour vérifier que vous avez obtenu les informations d’identification appropriées.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="6f9ee-113">L’exemple suivant montre comment appeler [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) pour demander à l’utilisateur un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="6f9ee-114">Il commence par remplir une structure CREDUI \_ info avec des informations sur les invites à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="6f9ee-115">Ensuite, le code remplit deux mémoires tampons avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="6f9ee-116">Cela permet de s’assurer qu’aucune information n’est transmise à la fonction qui peut révéler un ancien nom d’utilisateur ou mot de passe à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="6f9ee-117">L’appel à **CredUIPromptForCredentials** affiche la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="6f9ee-118">Pour des raisons de sécurité, cet exemple utilise l' \_ indicateur CREDUI Flags \_ do \_ not \_ Persist pour empêcher le système d’exploitation de stocker le mot de passe, car il peut être exposé.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="6f9ee-119">S’il n’y a pas d’erreur, **CredUIPromptForCredentials** remplit les variables PszName et pszPwd et retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="6f9ee-120">Lorsque l’application a terminé d’utiliser les informations d’identification, elle doit placer des zéros dans les tampons afin d’éviter que les informations ne soient révélées accidentellement.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a><span data-ttu-id="6f9ee-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f9ee-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f9ee-122">**CredUICmdLinePromptForCredentials**</span><span class="sxs-lookup"><span data-stu-id="6f9ee-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="6f9ee-123">**CREDUI \_ UINFO**</span><span class="sxs-lookup"><span data-stu-id="6f9ee-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
