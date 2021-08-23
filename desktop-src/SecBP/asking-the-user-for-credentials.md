---
description: Il se peut que votre application doive inviter l’utilisateur à entrer les informations de nom d’utilisateur et de mot de passe pour éviter de stocker un mot de passe administrateur ou pour vérifier que le jeton détient les privilèges appropriés.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Demande d’informations d’identification à l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9b9941be168a307e35b3575f4d12241dc624553686a61b232f2c5ba86e9c0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480489"
---
# <a name="asking-the-user-for-credentials"></a>Demande d’informations d’identification à l’utilisateur

Il se peut que votre application doive inviter l’utilisateur à entrer les informations de nom d’utilisateur et de mot de passe pour éviter de stocker un mot de passe administrateur ou pour vérifier que le jeton détient les privilèges appropriés.

Toutefois, il suffit de demander des informations d’identification pour former les utilisateurs à les fournir à une boîte de dialogue aléatoire, non identifiée, qui s’affiche à l’écran. La procédure suivante est recommandée pour réduire cet effet de formation.

**Pour acquérir correctement les informations d’identification de l’utilisateur**

1.  Informez l’utilisateur, en utilisant un message qui fait clairement partie de votre application, qu’il verra une boîte de dialogue qui demande son nom d’utilisateur et son mot de passe. Vous pouvez également utiliser la structure [**CREDUI \_ info**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) sur l’appel à [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) pour transmettre des données d’identification ou un message.
2.  Appelez [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa). Notez que le nombre maximal de caractères spécifié pour les informations de nom d’utilisateur et de mot de passe comprend le caractère null de fin.
3.  Appelez [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) et [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) pour vérifier que vous avez obtenu les informations d’identification appropriées.

L’exemple suivant montre comment appeler [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) pour demander à l’utilisateur un nom d’utilisateur et un mot de passe. Il commence par remplir une structure CREDUI \_ info avec des informations sur les invites à utiliser. Ensuite, le code remplit deux mémoires tampons avec des zéros. Cela permet de s’assurer qu’aucune information n’est transmise à la fonction qui peut révéler un ancien nom d’utilisateur ou mot de passe à l’utilisateur. L’appel à **CredUIPromptForCredentials** affiche la boîte de dialogue. Pour des raisons de sécurité, cet exemple utilise l' \_ indicateur CREDUI Flags \_ do \_ not \_ Persist pour empêcher le système d’exploitation de stocker le mot de passe, car il peut être exposé. S’il n’y a pas d’erreur, **CredUIPromptForCredentials** remplit les variables PszName et pszPwd et retourne zéro. Lorsque l’application a terminé d’utiliser les informations d’identification, elle doit placer des zéros dans les tampons afin d’éviter que les informations ne soient révélées accidentellement.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
